# Xiao Liu Menu Management System User Guide

## Project Address

Gitee Repository: [https://gitee.com/xiaaoke/menu-manager-wireless](https://gitee.com/xiaaoke/menu-manager-wireless)
GitHub Repository: [https://github.com/suipianma/menu-manager-wireless](https://github.com/suipianma/menu-manager-wireless)

## System Overview

Xiao Liu Menu Management System is a single-page application developed with HTML, CSS, and JavaScript for managing and maintaining dish menus. The system does not require a backend server and can run directly in a browser.

### Main Features
- Responsive design, adapting to various screen sizes
- Support for dark/light theme switching
- Complete dish management functionality
- Data backup and recovery
- Image upload and preview
- Powerful filtering and sorting capabilities

## Version Description

The system provides two versions, with `menu-manager-wireless.html` recommended as the priority:

### 1. menu-manager-wireless.html (Recommended)
- **Storage Method**: Uses IndexedDB for storage, with larger storage space (approximately 50MB)
- **File Operations**: Uses modern File System API for data import/export
- **Technical Features**: Uses modern JavaScript features like async/await
- **Error Tolerance**: More robust error handling and data migration mechanisms
- **Storage Limit**: Prompts users to export data when storage usage exceeds 80%

### 2. menu-manager.html (Traditional Version)
- **Storage Method**: Uses localStorage for storage, with smaller storage space (approximately 5MB)
- **File Operations**: Uses traditional file download methods for data backup
- **Technical Features**: Uses traditional JavaScript callback methods
- **Storage Limit**: localStorage has limited space, and large numbers of images may lead to insufficient storage

## System Functions

### 1. Dish Management

#### Add Dish
1. Click the "Add Dish" button at the top of the page
2. Fill in the following information in the pop-up form:
   - Dish name (required)
   - Price (required, must be greater than 0)
   - Category (Hot Dishes, Cold Dishes, Soups, Staples, Drinks)
   - Description (optional)
   - Image (optional, supports various image formats)
3. Click the "Add Dish" button to save

#### Edit Dish
1. Find the dish to edit in the dish list
2. Click the "Modify" button on the right side of the dish
3. Modify the corresponding information in the pop-up form
4. Click the "Save Changes" button to complete the edit

#### Delete Dish
1. Find the dish to delete in the dish list
2. Click the "Delete" button on the right side of the dish
3. Click the "OK" button in the confirmation dialog

### 2. Filtering and Searching

#### Search Function
- Enter dish name keywords in the search box, and the system will real-time filter matching dishes

#### Category Filter
- Select a specific category from the category dropdown menu, and the system will filter all dishes under that category
- Select "All Categories" to view all dishes

#### Sorting Function
- Sort by name in ascending/descending order
- Sort by price in ascending/descending order

### 3. Data Management

#### Export Data
1. Click the "Export Data" button at the bottom of the page
2. **menu-manager-wireless.html**: The system will open a file save dialog, select the save location
3. **menu-manager.html**: The system will generate a JSON format backup file and automatically download it
4. File name format: menu-backup-YYYY-MM-DD.json (traditional version) or menu-data.json (wireless version)

#### Import Data
1. Click the "Import Data" button at the bottom of the page
2. **menu-manager-wireless.html**: The system will open a file selection dialog, select the previously exported JSON file
3. **menu-manager.html**: Select the previously exported JSON backup file
4. The system will automatically import the data and refresh the page

### 4. Other Functions

#### Theme Switching
- Click the theme switching button (🌙/☀️) in the upper right corner of the page to switch between dark and light themes
- Theme settings are saved locally and will be automatically applied when opened next time

#### Image Preview
- Click on the dish image to view a large image in a modal box
- Click outside the modal box or the close button to close the preview

## Usage Guide

### First-time Use
1. **Recommended**: Open the `menu-manager-wireless.html` file directly in a browser
2. The system will automatically initialize and display an empty state prompt
3. Click the "Add Dish" button to start creating a menu

### Daily Use
1. **Add new dishes**: Use the "Add Dish" button
2. **Manage existing dishes**: Use the "Modify" and "Delete" buttons in the dish list
3. **Find dishes**: Use the search box and category filter
4. **Adjust display order**: Use the sorting function
5. **Regular backup**: Use the "Export Data" function to back up menu data

### Data Recovery
1. Click the "Import Data" button in the system
2. Select the previously exported backup file
3. The system will automatically import the data and refresh the page

## Technical Features

### menu-manager-wireless.html (Recommended)
- **Data Storage**: Uses IndexedDB for storage, with larger storage space (approximately 50MB)
- **Data Migration**: Automatically migrates data from localStorage to IndexedDB
- **File Operations**: Uses modern File System API for file operations
- **Error Handling**: More robust error handling mechanisms
- **Performance Optimization**: Uses async/await to improve code readability and performance

### menu-manager.html (Traditional Version)
- **Data Storage**: Uses localStorage for storage, with smaller storage space (approximately 5MB)
- **File Operations**: Uses traditional file download methods
- **Compatibility**: Supports older versions of browsers

### Common Features
- **Image Processing**: Supports uploading images as dish illustrations, automatically compresses images to save storage space
- **Responsive Design**: Adapts to desktop, tablet, and mobile devices
- **Real-time Operations**: Real-time filtering and sorting, no page refresh required
- **Local Storage**: Data is stored locally, no network requests required

## Notes

1. **Data Security**: Data is stored locally in the browser. Clearing browser data will cause menu data to be lost. Please regularly use the "Export Data" function to back up data.

2. **Storage Space**:
   - **menu-manager-wireless.html**: Uses IndexedDB, with larger storage space (approximately 50MB)
   - **menu-manager.html**: Uses localStorage, with limited storage space (approximately 5MB). Large numbers of images may occupy more space

3. **Image Size**: To ensure system performance and reasonable use of storage space, it is recommended not to upload overly large images. The system will automatically compress images.

4. **Browser Compatibility**:
   - **menu-manager-wireless.html**: Requires modern browsers that support IndexedDB and File System API
   - **menu-manager.html**: Supports more older versions of browsers

5. **Data Import**: Importing data will overwrite existing data. Please ensure you have backed up current data before importing.

## Troubleshooting

### Common Issues

1. **Unable to add dishes**
   - Check if the dish name and price have been filled in
   - Ensure the price is greater than 0

2. **Image upload failed**
   - Check if the image format is supported
   - Ensure the image size is reasonable

3. **Data loss**
   - Check if browser data has been cleared
   - Use previously exported backup files to restore data

4. **Insufficient storage space**
   - Export data and clear browser data
   - Reduce image usage or use smaller images
   - **Recommended**: Switch to the `menu-manager-wireless.html` version to get larger storage space

5. **Import/export failure**
   - Ensure the file format is correct (JSON format)
   - Check if the browser supports the corresponding file operation API
   - **menu-manager-wireless.html**: Ensure the browser supports File System API

### Contact Support

If you encounter other issues during use, please contact the system administrator for assistance.