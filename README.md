# NOT NFTPARIS - Event Calendar Website

A minimalistic black and white event calendar for NOT NFTPARIS with embedded Luma events.

## 🚀 Quick Start - Adding Events

Open `index.html` and find the **EVENT CONFIGURATION** section at the top of the script:

```javascript
// ========================================
// 📅 EVENT CONFIGURATION
// ========================================

const eventsByDate = {
    '02 Feb \'26': [
        'YOUR_EVENT_ID_1',
        'YOUR_EVENT_ID_2'
    ],
    '03 Feb \'26': [
        'YOUR_EVENT_ID_3'
    ],
    '04 Feb \'26': [
        'blogo4c2'
    ],
    '05 Feb \'26': [
        'YOUR_EVENT_ID_5',
        'YOUR_EVENT_ID_6'
    ],
    '06 Feb \'26': [
        'YOUR_EVENT_ID_7'
    ],
    '08 Feb \'26': [
        'YOUR_EVENT_ID_8'
    ]
};
```

### That's it! Just edit this section to manage all your events.

## 📝 How to Add/Edit Events

### Step 1: Get Your Luma Event ID

From your Luma event URL: `https://lu.ma/blogo4c2`
The event ID is: `blogo4c2`

### Step 2: Add to Configuration

```javascript
'04 Feb \'26': [
    'blogo4c2'           // Your event ID here
],
```

### Step 3: Multiple Events Same Day

```javascript
'02 Feb \'26': [
    'event-id-1',        // First event
    'event-id-2',        // Second event
    'event-id-3'         // Third event (no comma on last one)
],
```

### Step 4: Add a New Date

```javascript
'07 Feb \'26': [
    'your-new-event-id'
],
```

## ✏️ Examples

### Single Event Per Day
```javascript
'03 Feb \'26': [
    'abc123xyz'
],
```

### Multiple Events Per Day
```javascript
'05 Feb \'26': [
    'morning-event',
    'afternoon-event',
    'evening-event'
],
```

### Remove a Date
Just delete the entire date entry:
```javascript
// Remove this:
'06 Feb \'26': [
    'YOUR_EVENT_ID_7'
],
```

### Remove an Event
Just delete that event ID from the array:
```javascript
'02 Feb \'26': [
    'event-id-1',
    // 'event-id-2',    // Removed
    'event-id-3'
],
```

## 🎯 Date Format

**Important:** Use this exact format for dates:
```
'DD Mon \'YY'
```

Examples:
- `'02 Feb \'26'` ✅ Correct
- `'15 Mar \'26'` ✅ Correct
- `'01 Jan \'27'` ✅ Correct
- `'2 Feb 26'` ❌ Wrong
- `'02 February 2026'` ❌ Wrong

## 🔧 Customization

### Change Embed Height

Find this in the CSS section:
```css
.luma-embed-container iframe {
    height: 450px;  /* Change this value */
}
```

Adjust to:
- `400px` - Compact view
- `450px` - Default (current)
- `500px` - More room
- `600px` - Full view

### Change Card Width

```css
.day-column {
    min-width: 400px;  /* Change this value */
}
```

### Change Colors

```css
body {
    background-color: #000;  /* Background */
    color: #fff;             /* Text */
}
```

## ✨ Features

- ✅ Simple configuration - just list dates and event IDs
- ✅ Auto-generated calendar from config
- ✅ Full-screen horizontal layout
- ✅ Navigation arrows
- ✅ Multiple events per day stack vertically
- ✅ Direct Luma embeds with images and registration
- ✅ Minimalistic black & white theme
- ✅ Responsive design
- ✅ Auto-updating from Luma

## 🐛 Troubleshooting

### Event doesn't show up
- ✅ Check the event ID is correct
- ✅ Make sure the event is published on Luma
- ✅ Check for typos in the date format

### Iframe too tall/short
- Adjust the height in CSS (see Customization section)

### Arrows don't work
- Make sure you have multiple days that extend beyond screen width

### Date appears in wrong order
- The calendar displays dates in the order you list them in the config
- Organize your dates chronologically in the config

## 📱 Mobile Responsive

Automatically adjusts for mobile:
- Smaller columns (300px)
- Adjusted iframe height (400px)
- Touch-friendly arrows

## 💡 Pro Tips

1. **Keep event IDs organized** - Use descriptive Luma event names so IDs are easier to identify
2. **Test locally** - Open `index.html` in browser after each change
3. **Backup** - Keep a copy of your working config before making major changes
4. **Chronological order** - List dates in order for better UX

## 🎉 That's It!

No complex HTML editing needed. Just:
1. Get your Luma event IDs
2. Add them to the config
3. Refresh your browser

Happy event planning! 🚀
