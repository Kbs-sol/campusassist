# 📖 Campus Assistant Portal - User Manual

## 🎯 Welcome to Campus Assistant

Your comprehensive guide to using the Campus Assistant Portal - an AI-powered platform designed to help students navigate campus life, register for events, stay updated with notices, and get instant answers to campus-related questions.

---

## 👥 **FOR STUDENTS - How to Use the Portal**

### 🏠 Getting Started

1. **Visit the Portal**: Open your web browser and go to your campus assistant website
2. **Homepage Overview**: You'll see the main welcome screen with navigation options
3. **Navigation**: Click on any section in the top menu or use the buttons on the homepage

### 🤖 Using the AI Chatbot

#### Starting a Conversation
1. **Access Chat**: Click "Start Chat" on homepage or "Chat" in navigation menu
2. **Ask Questions**: Type your question in the text box at the bottom
3. **Send Message**: Press Enter or click the send button
4. **Wait for Response**: The AI will process your question (look for the loading animation)

#### What You Can Ask About
✅ **Campus Programs**: Admissions, courses, degree requirements  
✅ **Facilities**: Library, labs, hostels, dining, sports facilities  
✅ **Student Services**: Registration, fee payment, academic support  
✅ **Campus Life**: Clubs, activities, events, transportation  
✅ **Contact Information**: Department contacts, office hours, locations  

#### Example Questions
- "What are the admission requirements for Computer Science?"
- "Where is the library located and what are the timings?"
- "How do I register for courses next semester?"
- "What clubs and activities are available for students?"
- "Who can I contact for academic support?"

#### ❌ What the Chatbot Won't Answer
The AI is specifically designed for campus-related questions only. It will politely decline:
- Personal advice unrelated to campus
- General knowledge questions  
- Technical support for personal devices
- Non-academic topics

### 📅 Event Registration

#### Finding Events
1. **Navigate to Events**: Click "Events" in the main menu
2. **Browse Events**: Scroll through the list of upcoming campus events
3. **Event Details**: Click on any event to see full description, date, time, and location
4. **Filter Events**: Use category filters to find specific types of events

#### Registering for Events
1. **Choose Event**: Click "Register" button on the event you want to attend
2. **Fill Form**: Complete the registration form with your details:
   - Full Name (required)
   - Email Address (required)
   - Phone Number (optional but recommended)
   - Department/Course (if applicable)
   - Year of Study (if applicable)
   - Additional Information (special requirements, dietary restrictions, etc.)
3. **Submit**: Click "Register Now" to submit your registration
4. **Confirmation**: You'll receive an immediate confirmation on screen
5. **Email**: Check your email for a detailed confirmation with event details

#### Registration Confirmation Email
Your confirmation email will include:
- Event details (name, date, time, location)
- Your registration information
- Important notes and reminders
- Contact information for questions

### 📢 Campus Notices

#### Viewing Notices
1. **Navigate to Notices**: Click "Notices" in the main menu
2. **Browse All Notices**: Scroll through recent announcements
3. **Filter by Category**: Use the filter buttons to see specific types:
   - **Academic**: Course updates, exam schedules, academic deadlines
   - **Events**: Event announcements and updates
   - **General**: General campus information and updates
   - **Urgent**: Important time-sensitive announcements

#### Notice Information
Each notice includes:
- **Title**: Brief description of the announcement
- **Content**: Detailed information
- **Category**: Type of notice (Academic, Events, General, Urgent)
- **Date**: When the notice was published
- **Priority**: Importance level

### 📞 Contact & Feedback

#### Submitting Feedback
1. **Navigate to Contact**: Click "Contact" in the main menu
2. **Choose Feedback Type**: Select the type of feedback you want to provide
3. **Fill Form**: Complete the feedback form with your message
4. **Submit**: Click submit to send your feedback to campus administration

---

## 👨‍💼 **FOR ADMINISTRATORS - Managing the Portal**

### 🔐 Accessing Admin Panel

The admin panel is **intentionally hidden** from public view for security. There are **three ways** to access it:

#### Method 1: Keyboard Shortcut
1. **On Any Page**: Press `Shift + Alt + A` simultaneously
2. **Automatic Redirect**: You'll be taken to the admin login page immediately

#### Method 2: Secret URL
1. **Add Parameter**: Add `?VJ` to any URL (example: `yoursite.com?VJ`)
2. **Direct Path**: Or go directly to `/VJ` (example: `yoursite.com/VJ`)
3. **Automatic Redirect**: You'll be redirected to the admin login page

#### Method 3: Hidden Trigger
1. **Find the Corner**: Look for the bottom-left corner of any page
2. **Click Area**: Click in the very bottom-left corner (invisible 4x4 pixel area)
3. **Access Admin**: This will redirect you to the admin login page

### 🔑 Admin Login Process

1. **Admin Login Page**: Once redirected, you'll see the admin login form
2. **Enter API Key**: Input your `ADMIN_API_KEY` in the password field
3. **Sign In**: Click "Sign In" to authenticate
4. **Dashboard Access**: Upon successful login, you'll see the admin dashboard

### 📊 Admin Dashboard

#### Dashboard Overview
The admin dashboard provides:
- **Usage Statistics**: Number of chat sessions, popular questions
- **Event Metrics**: Registration counts, upcoming events
- **System Health**: API status, response times
- **Recent Activity**: Latest registrations and chat logs

#### Navigation Menu
- **Dashboard** - Main analytics overview
- **Events** - Manage campus events
- **Notices** - Manage announcements  
- **Chat Logs** - View AI conversations
- **System Status** - Monitor system health

### 📅 Event Management

#### Creating New Events
1. **Go to Events Section**: Click "Events" in admin menu
2. **Click "Create Event"**: Start creating a new event
3. **Fill Event Details**:
   - **Title**: Event name (e.g., "Campus Tech Fest 2024")
   - **Description**: Detailed event description
   - **Date & Time**: Event date and time in ISO format
   - **Location**: Venue information
   - **Category**: Event type (Academic, Cultural, Sports, etc.)
   - **Max Participants**: Maximum registration limit (optional)
4. **Save Event**: Click "Create Event" to publish

#### Editing Existing Events
1. **Find Event**: Locate the event in the events list
2. **Click Edit**: Click the edit button next to the event
3. **Modify Details**: Update any event information
4. **Save Changes**: Click "Update Event" to save modifications

#### Managing Registrations
1. **View Registrations**: Click "View Registrations" for any event
2. **Export Data**: Download registration list as CSV
3. **Send Reminders**: Send reminder emails to registered participants

### 📢 Notice Management

#### Creating New Notices
1. **Go to Notices Section**: Click "Notices" in admin menu
2. **Click "Create Notice"**: Start creating a new announcement
3. **Fill Notice Details**:
   - **Title**: Clear, descriptive title
   - **Content**: Full announcement text (supports HTML formatting)
   - **Category**: Notice type (Academic, Events, General, Urgent)
   - **Priority**: Importance level (Low, Medium, High)
   - **Expiration Date**: When notice should stop showing (optional)
4. **Publish Notice**: Click "Create Notice" to publish immediately

#### Notice Categories
- **Academic**: Course updates, exam schedules, academic deadlines
- **Events**: Event announcements and updates  
- **General**: General campus information and updates
- **Urgent**: Important time-sensitive announcements

#### Editing and Deleting Notices
1. **Find Notice**: Locate the notice in the notices list
2. **Edit**: Click edit button to modify content
3. **Delete**: Click delete button to remove notice (with confirmation)

### 🗨️ Chat Log Monitoring

#### Viewing Conversations
1. **Go to Chat Logs**: Click "Chat Logs" in admin menu
2. **Browse Sessions**: See all AI chat sessions with timestamps
3. **View Details**: Click on any session to see full conversation
4. **Filter Logs**: Filter by date, model used, or response time

#### Analytics Available
- **Popular Questions**: Most frequently asked questions
- **Model Performance**: Success rates for each AI model
- **Response Times**: Average response times
- **User Patterns**: Peak usage times and trends
- **Common Topics**: Categories of questions being asked

#### Using Chat Data
- **Improve Responses**: Identify questions that need better answers
- **Content Planning**: Create events/notices based on frequent questions
- **System Optimization**: Monitor AI model performance
- **User Support**: Identify areas where students need more help

### 🔧 System Management

#### System Health Monitoring
1. **Go to System Status**: Click "System Status" in admin menu
2. **Check Services**: View status of all integrated services:
   - Google Sheets Database
   - AI Services (Gemini, Groq, OpenRouter)
   - Email Service
   - System Performance
3. **View Logs**: Check error logs and system messages

#### Email Configuration Testing
1. **Test Email Setup**: Use "Test Email" function
2. **Send Test Message**: Send test email to verify configuration
3. **Check Results**: Confirm email delivery works correctly

### 📧 Email Notifications

#### Automatic Emails Sent
- **Registration Confirmations**: Sent immediately after event registration
- **Event Reminders**: Sent day before events (if configured)
- **Admin Notifications**: Sent to admin for new registrations

#### Email Template Management
- **Professional Templates**: Pre-designed email templates included
- **Campus Branding**: Generic campus assistant branding
- **Customizable Content**: Modify email content as needed

---

## 🛠️ **TROUBLESHOOTING GUIDE**

### 🤖 Chatbot Issues

#### "AI is unavailable" Message
**Problem**: Chatbot shows error message  
**Solutions**:
1. **Wait and Retry**: Try asking your question again in a few moments
2. **Check Internet**: Ensure you have stable internet connection
3. **Refresh Page**: Reload the webpage and try again
4. **Contact Admin**: If problem persists, contact campus administration

#### Slow Response Times
**Problem**: Chatbot takes long time to respond  
**Solutions**:
1. **Be Patient**: AI processing can take 5-15 seconds
2. **Check Connection**: Ensure stable internet connection
3. **Avoid Complex Questions**: Try breaking complex questions into simpler parts

#### Getting "Off-Topic" Responses
**Problem**: AI says it can only help with campus questions  
**Solutions**:
1. **Rephrase Question**: Make your question clearly campus-related
2. **Be Specific**: Ask about specific campus services, programs, or facilities
3. **Use Examples**: "How do I register for courses?" instead of "How do I register?"

### 📅 Event Registration Issues

#### Registration Form Won't Submit
**Problem**: "Register Now" button doesn't work  
**Solutions**:
1. **Check Required Fields**: Ensure name and email are filled correctly
2. **Valid Email**: Use a proper email format (e.g., student@email.com)
3. **Refresh Page**: Reload the page and try again
4. **Different Browser**: Try using a different web browser

#### Not Receiving Confirmation Email
**Problem**: No confirmation email in inbox  
**Solutions**:
1. **Check Spam Folder**: Look in spam/junk email folder
2. **Wait 10 Minutes**: Email delivery can take a few minutes
3. **Verify Email Address**: Ensure you typed email correctly during registration
4. **Contact Admin**: Reach out to confirm your registration

#### Event Shows "Full" or Registration Closed
**Problem**: Can't register because event is full  
**Solutions**:
1. **Waitlist**: Some events may have waitlist options
2. **Contact Organizers**: Reach out to event organizers directly
3. **Check for Similar Events**: Look for alternative events

### 📢 Notice Display Problems

#### Notices Not Loading
**Problem**: Notice section shows empty or loading continuously  
**Solutions**:
1. **Refresh Page**: Reload the webpage
2. **Check Internet**: Ensure stable internet connection
3. **Clear Browser Cache**: Clear your browser cache and cookies
4. **Try Later**: System might be temporarily unavailable

#### Filter Not Working
**Problem**: Category filters don't show correct notices  
**Solutions**:
1. **Refresh Page**: Reload and try filter again
2. **Check "All" First**: Click "All Notices" then try specific category
3. **Different Category**: Try different category filters to test

### 🔐 Admin Panel Issues

#### Can't Access Admin Login
**Problem**: Hidden triggers not working  
**Solutions**:
1. **Try All Methods**: Test all three access methods:
   - Keyboard: `Shift + Alt + A`
   - URL: Add `?VJ` to current URL  
   - Hidden area: Click bottom-left corner
2. **Clear Browser Cache**: Clear cache and try again
3. **Different Browser**: Try different web browser
4. **Check URL**: Ensure you're on the correct domain

#### Admin Login Fails
**Problem**: "Invalid API key" message  
**Solutions**:
1. **Check API Key**: Verify you have the correct `ADMIN_API_KEY`
2. **Copy-Paste**: Copy and paste the key to avoid typing errors
3. **Remove Spaces**: Ensure no extra spaces before/after the key
4. **Contact IT**: Verify the API key with your IT administrator

#### Admin Dashboard Not Loading
**Problem**: Blank screen after successful login  
**Solutions**:
1. **Wait for Loading**: Dashboard may take 10-15 seconds to load
2. **Refresh Page**: Reload the page after login
3. **Check Browser Console**: Press F12 and check for error messages
4. **Different Browser**: Try accessing admin panel in different browser

### 📊 Data Issues

#### Events/Notices Not Updating
**Problem**: New events or notices don't appear  
**Solutions**:
1. **Wait 5 Minutes**: Changes may take a few minutes to propagate
2. **Refresh Page**: Force refresh with Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)
3. **Check Admin Panel**: Verify data was saved correctly in admin panel
4. **Contact Admin**: Report persistent data sync issues

#### Registration Data Missing
**Problem**: Registration information not appearing in admin panel  
**Solutions**:
1. **Check Google Sheets**: Verify data appears in Google Sheets database
2. **Refresh Admin Panel**: Reload admin dashboard
3. **Check Date Filters**: Ensure date filters are set correctly
4. **Verify Permissions**: Confirm Google Sheets permissions are correct

---

## 📞 **GETTING HELP**

### 🎓 For Students
- **First Step**: Try the AI chatbot for quick answers
- **Campus IT**: Contact your campus IT support desk
- **Administration**: Reach out to student services or administration
- **Email Support**: Use the contact form on the portal

### 👨‍💼 For Administrators  
- **Technical Issues**: Contact your IT department or web administrator
- **API Problems**: Check environment variable configuration
- **Email Issues**: Verify SMTP settings and credentials
- **Database Issues**: Check Google Sheets permissions and service account

### 🚨 Emergency Contact
- **System Down**: Contact campus IT immediately
- **Security Concerns**: Report to campus security and IT
- **Data Issues**: Contact database administrator
- **Access Problems**: Verify with system administrator

---

## 🎯 **BEST PRACTICES**

### 👥 For Students
- **Be Specific**: Ask clear, campus-related questions to the AI
- **Check Email**: Always check spam folder for confirmations
- **Register Early**: Popular events fill up quickly
- **Stay Updated**: Check notices section regularly
- **Mobile Friendly**: Portal works great on mobile devices

### 👨‍💼 For Administrators
- **Regular Updates**: Keep events and notices current
- **Monitor Logs**: Check chat logs for common questions
- **Test Email**: Regularly test email functionality
- **Security**: Keep admin API key secure and private
- **Backup**: Regularly backup Google Sheets data
- **Monitor Performance**: Check system health regularly

### 🔐 Security Reminders
- **Admin Access**: Never share admin credentials
- **Secure Networks**: Access admin panel only from secure networks
- **Logout**: Always logout from admin panel when done
- **Regular Updates**: Keep system configurations updated

---

**📚 Campus Assistant Portal - Empowering Student Success**  
*Your complete guide to navigating campus life with AI assistance*