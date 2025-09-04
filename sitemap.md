# 🗺️ Campus Assistant Portal - Site Structure

## 📋 Overview
Complete site structure for the Campus Assistant Portal, including public pages, API endpoints, admin routes, and hidden access methods.

---

## 🌐 Public Pages

### Main Frontend Routes
- **`/`** - Homepage with welcome message, feature overview, and navigation
- **`/#home`** - Home section (default view)
- **`/#chat`** - AI Chatbot interface
- **`/#events`** - Event listings and registration
- **`/#notices`** - Campus notices and announcements
- **`/#contact`** - Contact form and feedback

### Static Assets
- **`/static/app.js`** - Main JavaScript application
- **`/static/styles.css`** - Custom CSS styles
- **`/static/style.css`** - Additional styling
- **`/robots.txt`** - Search engine directives (excludes admin routes)
- **`/sitemap.xml`** - Public sitemap for SEO

---

## 🔌 Public API Endpoints

### Core APIs
- **`GET /api/health`** - System health check and status
- **`POST /api/chat`** - AI chatbot interface with multi-model fallback
- **`GET /api/events`** - Retrieve campus events from Google Sheets
- **`GET /api/notices`** - Fetch campus notices with category filtering
- **`POST /api/register`** - Event registration with email confirmation

### API Features
- ✅ **Input Validation** - All inputs sanitized and validated
- ✅ **Rate Limiting** - Protection against abuse
- ✅ **CORS Security** - Restricted to site origin
- ✅ **Error Handling** - No stack traces in production

---

## 🔒 Hidden Admin Routes

### 🚫 **IMPORTANT: Admin routes are intentionally hidden from public discovery**

#### Admin Authentication
- **`/admin-login`** - Hidden login page (not linked publicly)
  - **Access Methods:**
    1. **Keyboard Shortcut**: `Shift + Alt + A`
    2. **Secret URL**: Add `?VJ` or `/VJ` to any URL
    3. **Hidden Trigger**: Invisible div in bottom-left corner
  - **Security**: Excluded from robots.txt and sitemap.xml

#### Admin API Routes (Require ADMIN_API_KEY)
- **`POST /api/admin/login`** - Admin authentication
- **`GET /api/admin/dashboard`** - Analytics and usage statistics
- **`GET /api/admin/chat-logs`** - View AI conversation logs
- **`POST /api/admin/events`** - Create new events
- **`PUT /api/admin/events/:id`** - Update existing events
- **`DELETE /api/admin/events/:id`** - Delete events
- **`POST /api/admin/notices`** - Create new notices
- **`PUT /api/admin/notices/:id`** - Update existing notices
- **`DELETE /api/admin/notices/:id`** - Delete notices
- **`GET /api/admin/registrations`** - View event registrations
- **`GET /api/admin/system-status`** - System health monitoring
- **`POST /api/admin/test-email`** - Test email configuration

---

## 🎯 Hidden Admin Access Methods

### 1. Keyboard Trigger
```javascript
// Activated by pressing Shift + Alt + A simultaneously
document.addEventListener('keydown', function(e) {
    if (e.shiftKey && e.altKey && e.key.toLowerCase() === 'a') {
        window.location.href = '/admin-login';
    }
});
```

### 2. Secret URL Parameters
- **Format**: `yoursite.com?VJ` or `yoursite.com/VJ`
- **Detection**: JavaScript checks URL for VJ parameter/path
- **Auto-redirect**: Immediately redirects to `/admin-login`

### 3. Invisible Trigger Element
```html
<!-- Hidden clickable area in bottom-left corner -->
<div id="hidden-admin-trigger" 
     class="fixed bottom-2 left-2 w-4 h-4 opacity-0 cursor-pointer" 
     onclick="triggerHiddenAdmin()" 
     title="Admin Access">
</div>
```

---

## 📊 Data Storage Architecture

### Google Sheets Database
- **Sheet ID**: Configured in `GOOGLE_SHEET_ID` environment variable
- **Authentication**: Google Service Account with JSON key

#### Sheet Structure:
1. **`events`** - Event management
   - Columns: `id`, `title`, `description`, `date_iso`, `location`, `category`, `max_participants`, `created_at`, `updated_at`

2. **`notices`** - Campus announcements
   - Columns: `id`, `title`, `content`, `category`, `priority`, `created_at`, `updated_at`, `expires_at`

3. **`registrations`** - Event registrations
   - Columns: `id`, `event_id`, `name`, `email`, `phone`, `department`, `year`, `additional_info`, `created_at`

4. **`chat_logs`** - AI conversation logs
   - Columns: `id`, `session_id`, `question`, `response`, `model_used`, `response_time`, `created_at`, `user_ip`

---

## 🔐 Security Architecture

### Frontend Security
- **No Admin Links**: Admin routes not visible in navigation
- **Hidden Triggers**: Multiple stealth access methods
- **Input Validation**: All forms validated client-side
- **XSS Protection**: Content sanitization

### Backend Security
- **API Authentication**: ADMIN_API_KEY for admin routes
- **Rate Limiting**: Protection against API abuse
- **CORS Restrictions**: Limited to site origin
- **Input Sanitization**: Server-side validation
- **Error Handling**: No stack traces exposed

### SEO Blocking
- **`robots.txt`**: Explicitly disallows admin routes
- **`sitemap.xml`**: Excludes admin pages
- **No Meta Tags**: Admin pages lack SEO optimization

---

## 🚀 Deployment Structure

### Cloudflare Pages (Primary)
```
dist/
├── index.html (generated from src/index.tsx)
├── static/
│   ├── app.js
│   ├── styles.css
│   └── style.css
├── robots.txt
└── sitemap.xml
```

### Build Process
1. **Vite Build**: `npm run build` → generates `dist/`
2. **Cloudflare Deploy**: `wrangler pages deploy dist`
3. **Environment**: Variables configured in Cloudflare dashboard

### Compatibility
- ✅ **Cloudflare Pages** - Primary deployment target
- ✅ **Vercel** - Compatible without changes
- ✅ **Netlify** - Compatible without changes

---

## 📱 Frontend Application Structure

### Single Page Application (SPA)
- **Framework**: Vanilla JavaScript (no React dependencies)
- **Styling**: Tailwind CSS (CDN) + Custom CSS
- **Icons**: FontAwesome (CDN)
- **State Management**: Global AppState object
- **Navigation**: Hash-based routing (`#home`, `#chat`, etc.)

### Key JavaScript Functions
- `showSection(sectionId)` - Navigate between sections
- `sendMessage()` - Handle chat interactions
- `loadEvents()` - Fetch and display events
- `loadNotices()` - Fetch and display notices
- `registerForEvent()` - Handle event registration
- `adminLogin()` - Admin authentication
- Hidden access triggers implementation

---

## 🎨 UI/UX Features

### Animations & Transitions
- **Page Transitions**: Smooth fade effects between sections
- **Card Hover Effects**: Elevated shadows on hover
- **Loading States**: Spinner animations for API calls
- **Toast Notifications**: Slide-in notifications
- **Form Validation**: Real-time error highlighting
- **Chat Bubbles**: Smooth message animations

### Responsive Design
- **Mobile-First**: Tailwind responsive classes
- **Breakpoints**: sm, md, lg, xl optimizations
- **Touch-Friendly**: Large click targets
- **Mobile Menu**: Collapsible navigation

---

## 🧪 Testing Endpoints

### Health Checks
```bash
# Basic health check
curl https://your-site.pages.dev/api/health

# Test chat (requires API keys)
curl -X POST https://your-site.pages.dev/api/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "Hello, what can you help me with?"}'

# Get events
curl https://your-site.pages.dev/api/events

# Get notices
curl https://your-site.pages.dev/api/notices
```

### Admin Testing (requires ADMIN_API_KEY)
```bash
# Admin login
curl -X POST https://your-site.pages.dev/api/admin/login \
  -H "Content-Type: application/json" \
  -d '{"api_key": "YOUR_ADMIN_KEY"}'

# Get dashboard (with auth header)
curl -H "Authorization: Bearer YOUR_ADMIN_TOKEN" \
  https://your-site.pages.dev/api/admin/dashboard
```

---

## 📋 Configuration Checklist

### Environment Variables Required
- ✅ `GEMINI_API_KEY` - Google Gemini AI
- ✅ `GROQ_API_KEY` - Groq AI (fallback)
- ✅ `OPENROUTER_API_KEY` - OpenRouter AI (final fallback)
- ✅ `GOOGLE_SHEET_ID` - Database sheet ID
- ✅ `GOOGLE_SERVICE_ACCOUNT_EMAIL` - Google service account
- ✅ `GOOGLE_SERVICE_ACCOUNT_PRIVATE_KEY` - Authentication key
- ✅ `ADMIN_API_KEY` - Admin panel security
- ✅ `SMTP_HOST` - Email server
- ✅ `SMTP_USER` - Email username
- ✅ `SMTP_PASS` - Email password
- ✅ `APP_BASE_URL` - Site base URL

### Post-Deployment Verification
1. **Public Site**: Visit homepage and test all sections
2. **API Health**: Check `/api/health` endpoint
3. **Chat Function**: Test AI chatbot with sample questions
4. **Events**: Verify event listings load correctly
5. **Notices**: Check notice filtering functionality
6. **Admin Access**: Test all three hidden access methods
7. **Admin Panel**: Verify login and dashboard functionality
8. **Email**: Test registration confirmation emails
9. **SEO**: Verify robots.txt and sitemap.xml accessibility
10. **Security**: Confirm admin routes blocked from search engines

---

**🎓 Campus Assistant Portal - Complete Site Architecture**  
*Every route, every trigger, every security measure documented*