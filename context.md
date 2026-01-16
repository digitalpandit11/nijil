# Multi-Tenant Travel Portal - Project Context

## Project Overview
A multi-tenant travel aggregator platform wireframe similar to Viator.com. This is a B2B2C model where:
- **Platform Admin** manages the entire system
- **Tenants (Tour Operators)** list their tour packages
- **End Users** browse and book tours from multiple operators

## Current Status: WIREFRAME PHASE
This is a **minimalistic HTML/CSS/JS wireframe** for client presentation. No backend implementation yet.

## Project Files
```
D:\RoughWork\Nijil\
├── travel-portal-wireframe.html   # Main wireframe file (single page)
├── context.md                      # This file
└── Multi-Tenant Travel Portal R1 5January2025.pdf   # Scope of work document
```

## Technology Stack (Wireframe)
- **Pure HTML5** - No frameworks
- **Pure CSS3** - Inline styles and `<style>` tag
- **Vanilla JavaScript** - For page navigation and interactivity
- **No Dependencies** - Can open directly in any browser

## Key Features Implemented

### 1. Public-Facing Pages
#### Home Page (`#home`) - Viator-Style Discovery UX
**Section Order:**
1. **Hero Search Section** - Dark gradient full-width hero with:
   - Labeled search fields (Destination, Date, Travelers, Category)
   - Trust statistics (500+ Experiences, 50+ Operators, 10K+ Travelers, 4.8 Rating)
2. **Experience Categories** - 6 category cards with icons, experience counts, hover effects
3. **Popular Experiences** - 4-column enhanced tour cards with:
   - Badges (Bestseller, Top Rated)
   - Wishlist buttons
   - Star ratings with review counts
   - Tenant attribution ("By {Tenant}")
   - Per-person pricing
4. **Why Book With Us** - 4 trust feature cards (Trusted Operators, Best Price Guarantee, Easy Booking, Free Cancellation)
5. **Trending Destinations** - 5 destination cards with gradient backgrounds and experience counts
6. **Footer CTA** - Sign-up call-to-action with footer links and copyright

#### Tours Listing Page (`#tours`)
- Filter options: Category, Price Range, Rating, Duration
- 6 tour packages in grid layout
- **Each tour shows:** Title, Tenant name ("By {Tenant}"), Rating, Reviews, Location, Description, Price

#### Tour Detail Modal
- Full tour information popup
- Displays: Tenant name, Image, Rating, Location, Duration
- Detailed itinerary (time-based schedule)
- What's included section
- Price and "Book Now" button

### 2. Admin Dashboard (`#admin-dashboard`)
**Sidebar Navigation:**
- 📊 Overview
- 🏢 Tenants
- 👥 Users/Customers
- 📦 Tour Packages
- 🗺️ Travel Itinerary
- 🏷️ Categories
- 📝 Bookings
- 💳 Payments
- 💬 Queries
- 💰 Price Markup
- 📈 Payout
- 📱 Social Media

**Key Sections:**

#### Overview Section
- 4 stats cards: Active Tenants (47), Total Bookings (1,234), Revenue ($84,290), Active Packages (89)
- **Most Popular Packages** table (Top 3 packages with tenant info, bookings, rating, revenue)
- **Most Viewed Packages** table (Top 5 packages with views count, conversion rate, category)
- **Best Rated Packages** table (Top 7 packages sorted by rating, with review count and category)

#### Tenants Section
- Complete tenant list table
- Shows: Tenant Name, Email, Package Count, Status, Join Date
- Add/Edit capabilities
- Sample tenants: Paradise Tours Co., European Travel Ltd., Desert Adventures

#### Users/Customers Section (NEW - View Only)
- **Stats Overview Cards:**
  - Total Users: 1,847
  - Users with Purchases: 1,234
  - Users with Wish Lists: 892
  - Total Customer Spend: $284,290
- **Advanced Filters:**
  - Filter by user type (All/With Purchases/With Wish Lists/New Users)
  - Sort by Recent Activity, Total Spend, Most Bookings, Join Date
  - Search by name or email
- **Users Table:** Shows user-wise data
  - User Name, Email, Total Purchases, Total Spend, Wish List Items, Last Activity, Joined Date
  - Actions: "Purchase History" and "Wish List" buttons
- **Purchase History Modal:** Complete booking history with stats
  - Summary: Total purchases, Total spend, Average order value
  - Full table of all bookings with Booking ID, Package, Tenant, Date, Amount, Status
- **Wish List Modal:** Saved packages with insights
  - Summary: Total items, Total value, Potential revenue indicator
  - Full table of wish list items with Package, Tenant, Category, Price, Rating
  - Marketing opportunity suggestions based on user interests
- **Read-only Notice:** Privacy policy reminder
- Sample data: 6 users with varied purchase history and wish lists

#### Tour Packages Section (COMPREHENSIVE)
- **Advanced Filters:**
  - Filter by Tenant (dropdown with all tenant names)
  - Filter by Category
  - Filter by Status (Active/Inactive/Pending Approval)
  - Search box
- **Table View:** 10 packages showing Package Name, Tenant, Category, Price, Bookings, Rating, Status, Actions
- **Card View:** Visual grid with tenant names prominently displayed
- **Actions:** View, Edit, Approve (for pending packages)
- **Admin has FULL ACCESS to ALL tenant packages**

#### Travel Itinerary Section (NEW)
- **Advanced Filters:**
  - Filter by Tenant
  - Filter by Package
  - Search box
- **Table View:** Shows Itinerary Name, Package, Tenant, Duration, Days, Created Date, Status, Actions
- **Actions:** View (detailed modal), Edit, Delete
- **Admin has FULL ACCESS to ALL tenant itineraries**
- Sample itineraries: Paris Complete City Tour, Bali Island Adventure, Desert Safari Experience, Swiss Mountain Expedition

#### Categories Section
- Complete category management table
- Shows: Category Name, Icon (emoji), Total Packages, Status, Created Date
- 7 categories implemented
- Add/Edit category functionality

#### Bookings Section
- Booking list with filters (Status, Date Range)
- Shows: Booking ID, Customer, Package, Date, Amount, Status
- Sample bookings with different statuses

#### Customer Queries Section (Multi-Platform - Enhanced)
- **Stats Overview:** Total Queries (156), Open (42), In Progress (28), Resolved (86)
- **Platform-wise Breakdown:** Clickable cards showing query counts by platform:
  - 🌐 Website (38)
  - 📘 Facebook (32)
  - 📸 Instagram (24)
  - ✉️ Email (28)
  - 💬 WhatsApp (18)
  - 📱 SMS (10)
  - 📞 Phone (6)
- **Response Metrics:** Urgent/SLA Breach (12), Avg Response Time (2.4 hrs), Resolution Rate (94%), Customer Satisfaction (4.6⭐)
- **Advanced Filters:** Platform, Status, Priority, Category, Search by ticket ID/customer
- **Queries Table:** 10 records with:
  - Ticket ID, Platform (color-coded badges), Customer (name + contact), Subject, Category, Priority (🔴🟠🟡🟢), Status, Created date with time ago, Assigned To, Actions (View/Reply/Reopen)
- **Priority Levels:** Urgent (red), High (orange), Medium (yellow), Low (green)
- **Status Types:** Open, In Progress, Awaiting Customer, Resolved, Closed
- **Categories:** Booking Issue, Payment Problem, Refund Request, Tour Information, Cancellation, Complaint, General Inquiry
- **Quick Actions:** Assign All Unassigned, Send Reminder to Pending, Generate Report, Configure SLA Rules
- **Pagination:** Shows 1-10 of 156 queries
- **View Query Modal:** Full query details with platform badge, customer info, subject, category, original message, related booking info, conversation thread, assignment tracking, internal notes, actions (assign, change status, reply)
- **Reply Query Modal:** Comprehensive response form with:
  - Query reference and customer details
  - Reply channel selection (WhatsApp/Email/SMS)
  - Quick response templates
  - Rich text response area with pre-filled example
  - Internal notes field
  - Status update dropdown
  - File attachments
  - Send/Draft actions

#### Price Markup Section (NEW)
- **Global Markup Settings Box:**
  - Default Platform Commission: 15%
  - Premium Tenant Rate: 10%
  - Special Category Rate: 12%
  - Edit buttons for each rate
- **Advanced Filters:**
  - Filter by Tenant
  - Filter by Category
  - Filter by Markup Type (Default/Custom/Premium)
  - Search functionality
- **Package Markup Table:** Shows all packages with pricing breakdown
  - Base Price (tenant's price)
  - Markup Percentage
  - Markup Amount (calculated)
  - Final Customer Price
  - Markup Type (Default/Premium/Special badge)
  - View and Edit actions
- **Summary Statistics:**
  - Total Platform Revenue from markup
  - Average Markup Rate
  - Packages with Custom Rates count
- Sample data: 7 packages with various markup configurations

### 3. Tenant Dashboard (`#tenant-dashboard`)
**Sidebar Navigation:**
- 📊 Overview
- 📦 My Packages
- 🗺️ Itineraries
- 📝 My Bookings
- 🏷️ Categories (View Only)
- 💰 Price Markup (View Only)
- 📈 Payouts (View Only)

**Key Sections:**

#### Tenant Overview
- 4 stats cards: Active Packages (12), Total Bookings (234), Revenue ($23,480), Avg Rating (4.7)
- Recent bookings table

#### Tour Packages (Full CRUD)
- **Stats Overview:** Total Packages, Active, Draft, Inactive counts
- **Performance Summary:** Total Bookings, Total Revenue, Avg Rating, Total Reviews
- **Advanced Filters:** Status, Category, Sort By, Search
- **Table View:** Package name with icon, Category, Price, Duration, Bookings, Rating, Status, Actions
- **Actions:** View, Edit, Delete for each package
- **Pagination:** Shows 8 packages per page with navigation
- **Add New Package button** opens comprehensive modal
- Sample packages: Paris City Explorer, French Wine Tour, London Royal Heritage, Italian Food Experience, Swiss Alps Adventure, Mediterranean Beach Escape, African Safari Premium, Rome Historical Tour

#### My Bookings (Enhanced)
- **Stats Overview:** Total Bookings (234), Confirmed (189), Pending (28), Cancelled (17)
- **Revenue Summary:** Total Revenue, Your Earnings, Avg Booking Value, Total Travelers
- **Advanced Filters:** Status, Package, Date Range, Search by booking ID or customer
- **Table View:** 10 bookings with Booking ID, Customer (name + email), Package, Travel Date, Travelers, Amount, Your Earnings, Status, View action
- **Pagination:** Shows 1-10 of 234 with page navigation
- **Upcoming Tours Alert:** Yellow notification showing tours scheduled for next 7 days
- **Export CSV button** for data export
- **View Booking Modal:** Complete booking details including package info, customer information, travel details, special requests, payment breakdown, earnings calculation, payment method, booking timeline

#### My Itineraries (NEW)
- **Filters:**
  - Filter by Package (tenant's own packages only)
  - Filter by Status
  - Search box
- **Table View:** Shows Itinerary Name, Package, Duration, Days, Created Date, Status, Actions
- **Actions:** View (detailed modal), Edit, Delete
- **Tenants can ONLY manage their own package itineraries**
- Sample itineraries: Paris Complete City Tour, French Countryside Wine Route, Royal London Heritage Walk

#### Categories (View Only - NEW)
- **Complete table view** showing all 7 platform categories
- Shows: Category Name, Icon, Total Packages, Status, Created Date
- **Action:** View button (opens category details modal)
- **Read-only access** - No Add/Edit/Delete options
- Blue info box explaining read-only access
- Categories: Beach & Islands, Adventure, Cultural, Food Tours, Art & Museums, Cruises, Wildlife Safari

#### Price Markup & Commission (View Only - NEW)
- **Your Markup Rate Summary Box:**
  - Applied Commission Rate: 15%
  - Total Revenue (Base): $1,029 (tenant's earnings)
  - Platform Commission: $182
- **My Package Pricing Table:** Complete pricing breakdown for tenant's packages
  - Your Base Price (what tenant set)
  - Platform Markup % (commission rate)
  - Markup Amount (commission in dollars)
  - Customer Price (final price)
  - Your Earnings/Booking (tenant receives base price)
  - View button (opens detailed modal)
- **How Pricing Works** - Green educational box explaining:
  - Base price, markup, customer price, earnings flow
  - Example calculation walkthrough
- **Read-only Notice** - Blue info box explaining rates are admin-controlled
- Sample data: 4 packages (Paris, French Wine Tour, London, Italian Food)

### 4. User Dashboard (`#user-dashboard`)
**Sidebar Navigation:**
- 🛒 Purchase History
- ❤️ Wish List
- 💬 My Queries
- 👤 Profile

**Key Sections:**

#### Purchase History
- Table showing all user bookings
- Includes: Booking ID, Package, Date, Travelers, Amount, Status, Actions
- View Details and Rate buttons

#### Wishlist
- Saved tours with tenant names
- Each card shows tenant ("By {Tenant}")
- Direct "Book Now" functionality

#### Queries
- User support ticket system
- Shows: Query ID, Subject, Package, Date, Status

## Role-Based Access Control (Per Scope Document)

| Feature | Admin | Tenant |
|---------|-------|--------|
| Tenant Management | All (CRUD) | View Only |
| Tour Packages | All (CRUD - ALL tenants) | All (CRUD - Own packages only) |
| Travel Itinerary | All | All |
| Tour Categories | All (CRUD) | View Only |
| Admin Dashboard | All | N/A |
| Bookings | View All | View Own |
| Payments | View All | N/A |
| Queries | View All | N/A |
| Price Markup | All (CRUD) | View Only |
| User Dashboard | View Only | N/A |
| Payout Calculation | All (CRUD) | View Only |
| Social Media Queries | All | N/A |

## Sample Data Implemented

### Tenants
1. Paradise Tours Co. (12 packages)
2. European Travel Ltd. (8 packages)
3. Desert Adventures (5 packages)
4. Asian Explorations
5. American Adventures Inc.

### Tour Packages
1. Paris City Explorer - $99 (European Travel Ltd.)
2. Bali Beach Getaway - $499 (Paradise Tours Co.)
3. Dubai Desert Safari - $149 (Desert Adventures)
4. New York Highlights - $129 (American Adventures Inc.)
5. London Royal Heritage - $159 (European Travel Ltd.)
6. Swiss Alps Adventure - $899 (European Travel Ltd.)
7. Tokyo Culture Tour - $189 (Asian Explorations)
8. African Safari - $1,299 (Paradise Tours Co.)
9. Italian Food Experience - $219 (European Travel Ltd.)
10. Greek Islands Cruise - $679 (Paradise Tours Co.)

### Categories
1. 🏖️ Beach & Islands (24 packages)
2. 🏔️ Adventure (18 packages)
3. 🏛️ Cultural (32 packages)
4. 🍽️ Food Tours (15 packages)
5. 🎨 Art & Museums (12 packages)
6. 🚢 Cruises (8 packages)
7. 🦁 Wildlife Safari (6 packages - Draft)

## Recent Work Completed

### Session 3 (2026-01-14)
1. ✅ **Enhanced Homepage to Viator-Style Discovery UX:**
   - **Hero Search Section:** Full-width dark gradient hero with improved search box (labeled fields for Destination, Date, Travelers, Category), trust stats (500+ Experiences, 50+ Operators, 10K+ Travelers, 4.8 Rating)
   - **Experience Categories:** 6 category cards with icons, hover effects, experience counts
   - **Popular Experiences:** 4-column tour grid with enhanced cards (badges like "Bestseller"/"Top Rated", wishlist button, star ratings, tenant attribution, per-person pricing)
   - **Why Book With Us (NEW):** 4-column trust feature grid (Trusted Operators, Best Price Guarantee, Easy Booking, Free Cancellation)
   - **Trending Destinations (NEW):** 5-column destination cards with gradient backgrounds, hover overlay effects, experience counts
   - **Footer CTA (NEW):** Full-width dark section with signup CTA, footer links (About, For Tour Operators, Help Center, Terms, Privacy, Contact), copyright
   - Added comprehensive CSS styles and mobile responsive breakpoints for all new sections

2. ✅ **Implemented Viator-Style Mega Menu:**
   - **Trigger:** "Discover" nav item with dropdown arrow, opens on hover
   - **Layout:** Full-width dropdown (100vw), white background, subtle shadow
   - **Top Tabs (3):** Top activities (default), Top landmarks, Explore the world
   - **Left Category List (6 per tab):** Vertical list with arrow indicator (›), highlights on hover
     - Activities: Top categories, Middle East & Africa, Asia, Caribbean, Europe, North America
     - Landmarks: Iconic, Museums, Natural wonders, Historical, Religious, Modern architecture
     - Explore: By continent, Trending, Beach, City breaks, Adventure, Romantic
   - **Right Content Area:** 3-column grid of destination/activity links, dynamically updates on category hover
   - **Interactions:** Tab switching, category hover updates right content, visual highlighting
   - **Accessibility:** Semantic HTML (role attributes), keyboard navigation support, focus styles
   - **JavaScript Functions:** `switchMegaTab()`, `showMegaCategory()`, keyboard event handlers

3. ✅ **Converted Tour Detail to Full Independent Page (`#tour-detail`):**
   - **NOT a modal/popup** - Full page layout that scrolls normally
   - **Image Gallery Section:** 2-column grid (main + 2 thumbnails), "View all 12 photos" button
   - **Tour Title & Meta:** H1 title, star rating, review count, booking count, location
   - **Operator Section:** Avatar with initials, name, verified badge, years on platform, avg rating, TOP RATED/Superhost badges
   - **Two-Column Layout:**
     - **LEFT (Scrollable):** Highlights, Description, Quick Info (4-col grid), Itinerary Timeline, Inclusions/Exclusions, Cancellation Policy
     - **RIGHT (Sticky Booking Card):** Date selector, Travelers (+/- controls), Price per person, Total calculation, Book Now button, Trust notes
   - **Related Experiences:** 4-column grid of similar tours
   - **Navigation Change:** All tour cards now use `showPage('tour-detail')` instead of `openTourModal()`
   - **JavaScript:** `updateTravelers()` function for booking card traveler count and price calculation
   - **Mobile:** Gallery stacks, booking card becomes sticky bottom bar, content stacks vertically

4. ✅ **Implemented Admin Payout Calculation (Full CRUD):**
   - **Stats Overview:** Total Payouts (This Month), Pending Payouts, Payouts Processed, Avg Platform Commission
   - **Payout Settings Summary:** Payout Cycle, Minimum Payout, Payment Method, Processing Time
   - **Filters:** By Tenant, Status (Pending/Processing/Completed/Failed), Date Range, Search by Payout ID
   - **Payout Table:** Payout ID, Tenant, Period, Total Bookings, Gross Revenue, Commission, Net Payout, Status, Actions
   - **Actions:** View, Edit, Delete buttons for each payout record
   - **Tenant Summary Table:** Per-tenant breakdown showing Total Bookings, Gross Revenue, Commission, Paid, Pending, Payment Method
   - **View Payout Modal:** Full payout details with tenant info, financial breakdown, booking details, payment information, download receipt
   - **Add/Edit Payout Modal:** Tenant selection, period dates, auto-calculated values, commission rate, payment method, status, notes
   - Sample data: 8 payout records across 5 tenants with various statuses

5. ✅ **Implemented Tenant Payout (View-Only):**
   - **Stats Overview:** Total Earnings, Platform Commission, Net Payout, Pending Payout
   - **Payout Settings:** Commission rate, payout cycle, payment method, bank account (masked)
   - **Next Scheduled Payout:** Date and estimated amount highlighted
   - **Payout History Table:** View-only with Payout ID, Period, Bookings, Gross, Commission, Net, Status
   - **View Tenant Payout Modal:** Earnings breakdown, bookings by package, payment details
   - **How Payouts Work:** Educational section explaining the payout process
   - Read-only notice with support contact option

6. ✅ **Implemented Admin Payment List:**
   - **Stats Overview:** Total Revenue, Total Transactions, Avg Transaction Value, Success Rate
   - **Payment Methods Breakdown:** Credit Card, PayPal, Bank Transfer, Apple/Google Pay with percentages
   - **Filters:** By Status, Payment Method, Tenant, Date Range, Search by Transaction ID
   - **Payment Transactions Table:** 10 records with Transaction ID, Date/Time, Customer (name + email), Package, Tenant, Amount, Method (color-coded badges), Status, View action
   - **Recent Refunds Table:** Refund ID, Original Transaction, Customer, Package, Amount, Reason, Date, Status
   - **View Payment Modal:** Full transaction details with customer info, booking details, payment breakdown, payment method, revenue split (tenant vs platform)

7. ✅ **Enhanced Tenant Tour Packages (Full CRUD):**
   - **Stats Overview:** Total Packages (12), Active (9), Draft (2), Inactive (1)
   - **Performance Summary:** Total Bookings (547), Total Revenue ($48,230), Avg Rating (4.7), Total Reviews (892)
   - **Advanced Filters:** Status filter, Category filter, Sort options (Newest, Most Bookings, Highest Rated, Price), Search
   - **Table View:** Package with icon, Category, Price, Duration, Bookings, Rating, Status, Actions (View/Edit/Delete)
   - **8 Sample Packages:** Paris City Explorer, French Wine Tour, London Royal Heritage, Italian Food Experience, Swiss Alps Adventure, Mediterranean Beach Escape (Draft), African Safari Premium (Draft), Rome Historical Tour (Inactive)
   - **Pagination:** Shows 1-8 of 12 packages with page navigation
   - **Enhanced Add/Edit Package Modal:** Comprehensive form with sections:
     - Basic Information: Name, Category, Status, Short/Full Description
     - Pricing & Duration: Base Price, Discounted Price, Currency, Duration Type, Number of Days
     - Location & Logistics: Destination, Meeting Point, Min/Max Participants
     - Package Details: Highlights, What's Included/Excluded
     - Policies: Cancellation Policy, Additional Notes
     - Images: Emoji icon, Image upload with drag-and-drop placeholder
     - Action buttons: Cancel, Save as Draft, Create Package
   - **View Package Modal:** Complete package details including:
     - Header with icon, name, status, quick stats (price, rating, bookings, revenue)
     - Quick stats grid: Created date, Last Updated, Min/Max Guests, Availability
     - Description, Highlights grid, Inclusions/Exclusions lists
     - Meeting Point, Cancellation Policy info boxes
     - Recent Bookings table (last 3 bookings with customer, date, guests, amount, status)
     - Actions: Close, Edit Package, Delete Package

8. ✅ **Enhanced Tenant Bookings Section:**
   - **Stats Overview:** Total Bookings (234), Confirmed (189), Pending (28), Cancelled (17)
   - **Revenue Summary:** Total Revenue ($23,480), Your Earnings ($19,958), Avg Booking Value ($100.34), Total Travelers (412)
   - **Advanced Filters:** Status (Confirmed/Pending/Completed/Cancelled/Refunded), Package selection, Date range, Search
   - **Bookings Table:** 10 records with Booking ID, Customer (name + email), Package with icon, Travel Date, Travelers, Amount, Your Earnings (green), Status, View action
   - **Pagination:** Shows 1-10 of 234 bookings
   - **Upcoming Tours Alert:** Yellow notification box showing next 7 days scheduled tours
   - **Export CSV button** for data export
   - **View Tenant Booking Modal:** Comprehensive booking details with:
     - Booking header with ID, date, status
     - Package info card with icon, name, duration, category, price
     - Customer information: Name, Email, Phone, Country
     - Travel details: Date, Start Time, Travelers
     - Special Requests highlighted box
     - Payment breakdown: Package price, Service fee, Total paid
     - Earnings breakdown: Your earnings, Platform commission (green highlight)
     - Payment method and status
     - Booking timeline with status indicators
     - Actions: Close, Contact Customer, Download Voucher

9. ✅ **Implemented Multi-Platform Customer Queries (Admin):**
   - **Stats Overview:** Total Queries (156), Open (42), In Progress (28), Resolved (86)
   - **Platform-wise Breakdown:** 7 clickable platform cards with query counts:
     - Website (38), Facebook (32), Instagram (24), Email (28), WhatsApp (18), SMS (10), Phone (6)
   - **Response Metrics:** Urgent/SLA Breach count, Avg Response Time, Resolution Rate, Customer Satisfaction
   - **Advanced Filters:** Platform, Status, Priority, Category, Search
   - **Queries Table:** 10 sample queries from various platforms with:
     - Color-coded platform badges (WhatsApp green, Facebook blue, Instagram pink, etc.)
     - Priority indicators (🔴 Urgent, 🟠 High, 🟡 Medium, 🟢 Low)
     - Status badges (Open, In Progress, Awaiting Customer, Resolved, Closed)
     - SLA breach highlighting (red background for urgent open tickets)
     - Assignment tracking and time-since-created display
   - **Quick Actions:** Bulk assign, Send reminders, Generate reports, Configure SLA
   - **View Query Modal:** Complete query details with:
     - Platform badge and customer contact info
     - Subject, category, original message with platform timestamp
     - Related booking/package information
     - Conversation thread with responses
     - Assignment and SLA tracking
     - Internal notes section
     - Quick actions: Assign, Change Status, Reply
   - **Reply Query Modal:** Full response functionality with:
     - Query reference and customer preview
     - Multi-channel reply selection (WhatsApp, Email, SMS)
     - Quick response templates dropdown
     - Rich text response area with pre-populated example
     - Internal notes (not visible to customer)
     - Status update after reply
     - File attachments with drag-and-drop
     - Send/Save Draft actions

### Session 2 (2026-01-13)
1. ✅ Added date selection and travelers count to Tours Listing page filters
2. ✅ Added View and Delete options to Admin Tenant Management
3. ✅ Created "View Tenant" modal with comprehensive tenant details
4. ✅ Added Delete option to Admin Tour Packages (both table and card views)
5. ✅ **Implemented Travel Itinerary Management:**
   - Added Travel Itinerary section to Admin Dashboard
   - Added Travel Itinerary section to Tenant Dashboard
   - Created "View Itinerary" modal with detailed day-by-day schedule
   - Created "Add/Edit Itinerary" modal with comprehensive form
   - Full CRUD operations: Add, View, Edit, Delete for both Admin and Tenant
   - Admin can manage itineraries across ALL tenants
   - Tenants can only manage their own package itineraries
   - Filters by tenant, package, and status
6. ✅ **Implemented Tenant Categories (View-Only):**
   - Complete table view showing all 7 categories
   - View button opens category details modal
   - Read-only access with informative message
   - Shows category description and popular destinations
   - No Add/Edit/Delete options for tenants
7. ✅ **Enhanced Admin Dashboard Overview:**
   - Added "Most Viewed Packages" table (5 packages with views, conversion rate)
   - Added "Best Rated Packages" table (7 packages sorted by rating with reviews)
8. ✅ **Implemented Price Markup Management:**
   - Global Markup Settings with 3 rate tiers (Default 15%, Premium 10%, Special 12%)
   - Complete package markup table showing pricing breakdown
   - Base Price → Markup % → Markup Amount → Final Price calculation
   - Markup type badges (Default/Premium/Special)
   - Filters by Tenant, Category, and Markup Type
   - View Markup modal with complete revenue analytics
   - Add/Edit Markup modal with live price calculation preview
   - Global Settings modal to configure platform-wide rates
   - Summary statistics showing total revenue, average rate, custom packages count
9. ✅ **Implemented Tenant Price Markup (View-Only):**
   - Summary box showing tenant's commission rate, revenue, and platform commission
   - Complete pricing table for tenant's packages
   - Shows base price, markup %, markup amount, customer price, earnings per booking
   - "How Pricing Works" educational section with example
   - View modal with detailed earnings breakdown per package
   - Read-only access with informative notice
10. ✅ **Implemented Users/Customers Management (View-Only):**
   - Added Users/Customers menu to Admin sidebar
   - Stats overview: Total users, Users with purchases, Users with wish lists, Total customer spend
   - Comprehensive user table showing purchase behavior and wish list activity
   - Filters by user type and sorting options
   - Purchase History modal with complete booking history and spend analytics
   - Wish List modal with saved packages and marketing opportunity insights
   - Privacy-conscious read-only access with notice

### Session 1 (2026-01-12)
1. ✅ Read project scope document
2. ✅ Analyzed Viator.com concept
3. ✅ Created complete wireframe structure
4. ✅ Implemented all 5 main pages (Home, Tours, Admin, Tenant, User dashboards)
5. ✅ Added comprehensive Admin Tour Packages section with:
   - Table view with all tenant packages
   - Card view option
   - Advanced filtering (Tenant, Category, Status)
   - Search functionality
   - Edit/View/Approve actions
6. ✅ Implemented Categories management section
7. ✅ Added "By {Tenant Name}" to ALL tour cards across the platform:
   - Home page popular tours
   - Tours listing page
   - User wishlist
   - Tour detail modal
8. ✅ Created this context document

### Visual Design
- Modern, clean interface
- Blue color scheme (#2563eb primary)
- Gradient cards for stats
- Responsive grid layouts
- Modal popups for forms and details
- Badge system for status indicators (Active/Pending/Success/Warning)
- Hover effects on cards
- Emoji icons for visual appeal

## Navigation Structure

```
Home (#home)
├── Hero with Search
├── Categories Grid
└── Popular Tours

Tours (#tours)
├── Filters
└── All Tours Grid

Tour Detail (#tour-detail)
├── Image Gallery
├── Title & Meta
├── Operator Section
├── Two-Column Layout (Content + Sticky Booking Card)
└── Related Experiences

Admin Dashboard (#admin-dashboard)
├── Overview (default)
├── Tenants Management
├── Tour Packages (ALL tenants)
├── Categories Management
├── Bookings
├── Payments
├── Queries
├── Price Markup
├── Payout Calculation
└── Social Media

Tenant Dashboard (#tenant-dashboard)
├── Overview (default)
├── My Packages
├── Itineraries
├── My Bookings
├── Categories (View Only)
├── Price Markup (View Only)
└── Payouts (View Only)

User Dashboard (#user-dashboard)
├── Purchase History (default)
├── Wish List
├── My Queries
└── Profile
```

## JavaScript Functions Implemented

```javascript
showPage(pageName)              // Main page navigation (includes 'tour-detail')
showAdminSection(sectionName)   // Admin dashboard section switching
showTenantSection(sectionName)  // Tenant dashboard section switching
showUserSection(sectionName)    // User dashboard section switching
openModal(modalId)              // Open modal popup
closeModal(modalId)             // Close modal popup
switchMegaTab(tabName)          // Switch mega menu top tabs
showMegaCategory(tabName, cat)  // Show category links in mega menu
updateTravelers(change)         // Tour detail booking card traveler count
```

## Modals Implemented
1. ~~**Tour Detail Modal**~~ → **Converted to Full Page** (`#tour-detail`) - See Navigation Structure
2. **View Tenant Modal** (`#view-tenant`) - Shows comprehensive tenant details with revenue, bookings, ratings
3. **Add Tenant Modal** (`#add-tenant`) - Form to add new tenant
4. **Add Package Modal** (`#add-package`) - Form to add new tour package
5. **Add Category Modal** (`#add-category`) - Form to add new category
6. **View Category Modal** (`#view-category`) - Shows category details with description, package count, popular destinations (read-only for tenants)
7. **View Itinerary Modal** (`#view-itinerary`) - Shows detailed day-by-day itinerary with schedule, inclusions
8. **Add/Edit Itinerary Modal** (`#add-itinerary`) - Comprehensive form for creating/editing itineraries
9. **Add/Edit Markup Rule Modal** (`#add-markup`) - Form to set/edit markup rates for packages with price calculation preview
10. **View Markup Details Modal** (`#view-markup`) - Shows complete markup breakdown with revenue calculations (Admin)
11. **Edit Global Markup Settings Modal** (`#edit-global-markup`) - Configure platform-wide default markup rates
12. **View Tenant Markup Modal** (`#view-tenant-markup`) - Read-only pricing details for tenants showing earnings and commission breakdown
13. **View User Purchase History Modal** (`#view-user-purchases`) - Complete purchase history for individual users with booking details and spend analytics
14. **View User Wish List Modal** (`#view-user-wishlist`) - User's saved packages with marketing insights and potential revenue analysis
15. **View Payout Modal** (`#view-payout`) - Full payout details with tenant info, financial breakdown, booking details, payment information
16. **Add/Edit Payout Modal** (`#add-payout`) - Form to create/edit payouts with tenant selection, period, commission calculation, status
17. **View Tenant Payout Modal** (`#view-tenant-payout`) - Read-only payout details for tenants showing earnings breakdown, bookings by package, payment info
18. **View Payment Modal** (`#view-payment`) - Full transaction details with customer info, booking details, payment breakdown, revenue split
19. **View Package Modal** (`#view-package`) - Comprehensive package details for Tenant with stats, description, highlights, inclusions, recent bookings, and action buttons
20. **View Tenant Booking Modal** (`#view-tenant-booking`) - Complete booking details for Tenant with customer info, travel details, payment breakdown, earnings calculation, timeline
21. **View Query Modal** (`#view-query`) - Full query details with platform info, customer contact, original message, conversation thread, assignment tracking, internal notes
22. **Reply Query Modal** (`#reply-query`) - Multi-channel response form with templates, rich text editor, internal notes, status update, file attachments

## Important Design Decisions

### Multi-Tenancy Display
- **User Perspective:** Users see "By {Tenant Name}" on every package to know the tour operator
- **Admin Perspective:** Admin sees tenant names in tables and can filter/manage all packages
- **Tenant Perspective:** Tenants only see and manage their own packages

### Color Coding
- **Primary Blue (#2563eb):** Main actions, tenant names, links
- **Success Green:** Active status, confirmed bookings
- **Warning Yellow:** Pending approvals, draft items
- **Info Blue:** Completed bookings

### Responsive Design
- Grid layouts adapt to screen size
- Mobile breakpoint at 768px
- Stacked layouts on mobile
- Collapsible navigation on small screens

## What's NOT Implemented (Future Phases)

### Backend Requirements
- Database design
- User authentication system
- Payment gateway integration
- Booking system logic
- Email/WhatsApp notifications
- Social media API integration (FB/Instagram leads)
- Image upload functionality
- Real-time search
- Booking calendar/availability
- Price markup calculation engine
- Payout calculation system

### Frontend Enhancements (Future)
- Image galleries for tours
- Interactive maps for locations
- Date range picker
- Real filtering logic
- Form validation
- AJAX/API calls
- Pagination
- Sorting functionality
- Advanced search
- User reviews/ratings interface
- Booking checkout flow
- Payment forms

## How to Use This Wireframe

### For Client Presentation
1. Open `travel-portal-wireframe.html` in any modern browser
2. Navigate through different sections using top navigation
3. Click on tour cards to see detail modal
4. Use sidebar navigation in dashboards
5. Demonstrate role-based views (Admin/Tenant/User)

### For Development Team
1. This wireframe serves as the UI/UX reference
2. All features shown here need backend implementation
3. Database schema should support multi-tenancy
4. APIs needed for each CRUD operation
5. Authentication system must support 3 user roles

## Next Steps (When Development Begins)

1. **Database Design**
   - Users table (with role: admin/tenant/user)
   - Tenants table
   - Categories table
   - Packages table (with tenant_id foreign key)
   - Bookings table
   - Payments table
   - Queries table
   - Itineraries table
   - Price_markup table
   - Payout_calculations table

2. **Backend API Endpoints**
   - Authentication (/login, /register, /logout)
   - Tenants CRUD
   - Packages CRUD (with multi-tenant filter)
   - Categories CRUD
   - Bookings CRUD
   - Search & Filter
   - Payment processing
   - Query management
   - Social media integration

3. **Frontend Framework Selection**
   - React/Vue/Angular for SPA
   - Next.js for SSR
   - Or continue with vanilla JS

4. **Infrastructure**
   - Hosting platform
   - Database (PostgreSQL/MySQL)
   - File storage (AWS S3 for images)
   - CDN for static assets

## Key Contact Info
- **Project Name:** Multi-Tenant Travel Portal
- **Project Phase:** R1 - Wireframe
- **Document Date:** January 5, 2025
- **Wireframe Created:** January 12, 2026
- **Reference Site:** Viator.com

## Notes
- This is a **PRESENTATION WIREFRAME** - no actual functionality
- All data is static/sample data
- Buttons and forms don't submit anywhere
- Search and filters are visual only
- Focus on demonstrating the multi-tenant concept
- Emphasize clear tenant attribution on all packages
- Admin has full visibility to all tenant packages

---
**Last Updated:** January 14, 2026
**Status:** Wireframe Complete ✅
**Next Phase:** Client Approval → Development Planning
