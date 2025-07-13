# ToDo Application - Mobile Test Automation

A comprehensive mobile test automation suite for a ToDo application using Katalon Studio and Appium.

## 📋 Project Overview

This project contains automated test cases for a mobile ToDo application, covering both positive and negative test scenarios. The test suite is built using Katalon Studio and targets Android mobile applications.

## 🚀 Prerequisites

### Software Requirements
- **Katalon Studio** (Latest version)
- **Appium Server** (for mobile automation)
- **Android SDK** 
- **Java Development Kit (JDK)** 8 or higher
- **Node.js** (for Appium dependencies)

### Mobile Device Requirements
- Android device or emulator
- Android version 7.0 or higher
- USB debugging enabled (for real devices)

## 📁 Project Structure

```
silver-octo-bassoon/
├── Object Repository/          # UI element locators
│   ├── android.widget.Button - [Actions]
│   ├── android.widget.EditText - [Input Fields]
│   ├── android.widget.TextView - [Display Elements]
│   ├── delete all/            # Delete all functionality elements
│   └── negative case/         # Negative test case elements
├── Test Cases/                # Test case definitions
│   ├── Positive Case/         # Valid scenarios
│   └── Negative Case/         # Invalid scenarios
├── Scripts/                   # Groovy test scripts
│   ├── Positive Case/
│   └── Negative Case/
├── Profiles/                  # Execution profiles
├── settings/                  # Project configuration
└── Reports/                   # Test execution reports
```

## 🧪 Test Scenarios

### Positive Test Cases
1. **Create Task with Valid Data**
   - Creates a new task with valid title and content
   - Verifies task is successfully saved

2. **Update Existing Task with Valid Data**
   - Modifies an existing task with new information
   - Confirms changes are saved correctly

3. **Delete Task with Valid Data**
   - Removes a specific task from the list
   - Validates task is deleted successfully

4. **Delete All Tasks**
   - Removes all tasks from the application
   - Confirms all tasks are cleared

### Negative Test Cases
1. **Create Task Without Task Title**
   - Attempts to create task with empty title
   - Validates error message: "Title is Empty"

2. **Create Task Without Task Content**
   - Attempts to create task with empty content
   - Validates error message: "Content is Empty"

3. **Create Task Without Title and Content**
   - Attempts to create task with both fields empty
   - Validates appropriate error handling

## 🔧 Setup Instructions

### 1. Environment Setup
```bash
# Install Node.js dependencies for Appium
npm install -g appium
npm install -g appium-doctor

# Verify Appium installation
appium-doctor --android
```

### 2. Android Setup
- Install Android SDK
- Set up ANDROID_HOME environment variable
- Enable USB debugging on target device
- Install the ToDo application on the device

### 3. Katalon Studio Configuration
1. Open Katalon Studio
2. Import this project
3. Configure mobile settings in Project → Settings → Mobile
4. Set up desired capabilities for your Android device

### 4. Appium Server Configuration
```bash
# Start Appium server
appium

# Default server runs on: http://localhost:4723/wd/hub
```

## ▶️ How to Run Tests

### Running Individual Test Cases
1. Open Katalon Studio
2. Navigate to **Test Cases** folder
3. Right-click on desired test case
4. Select **Run** → **Android**

### Running Test Suites
1. Create a Test Suite in Katalon Studio
2. Add test cases to the suite
3. Execute the entire suite

### Command Line Execution
```bash
# Run specific test case
katalon -projectPath="path/to/project" -testCasePath="Test Cases/Positive Case/create task with valid data"

# Run all test cases
katalon -projectPath="path/to/project" -testSuitePath="Test Suites/All Tests"
```

## 📱 Mobile Application Features Tested

### Core Functionality
- ✅ Task creation with title and content
- ✅ Task editing and updates
- ✅ Individual task deletion
- ✅ Delete all tasks functionality
- ✅ Task list display and navigation

### UI Elements Tested
- **Input Fields**: Task title, task content
- **Buttons**: Save, Edit, Delete, Update, Cancel
- **Navigation**: Image buttons for navigation
- **Display**: Task lists, error messages
- **Dialogs**: Delete confirmation dialogs

## 🔍 Object Repository Details

### Key UI Elements
- **EditText Fields**: Task title and content input
- **Buttons**: Action buttons (Save, Edit, Delete, Update)
- **TextView**: Display elements and error messages
- **ImageButton**: Navigation elements
- **RecyclerView**: Task list container
- **LinearLayout**: Layout containers

## 📊 Test Data and Validation

### Sample Test Data
- **Valid Task Title**: "To do list hari ini"
- **Valid Task Content**: "task hari ini tanggal 03012024"
- **Date References**: "tanggal 04012024", "20 Januari 2024"

### Validation Points
- Error message verification
- Task creation confirmation
- Task update validation
- Deletion confirmation
- Empty field handling

## 🐛 Known Issues and Limitations

- Tests are designed for Android platform only
- Requires stable network connection for Appium
- Device-specific UI elements may need adjustment
- Screen resolution dependencies may affect element location

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Add new test cases or improve existing ones
4. Follow Katalon Studio best practices
5. Submit a pull request

## 📝 Best Practices

### Test Case Development
- Use descriptive names for test cases
- Implement proper wait strategies
- Handle dynamic elements appropriately
- Include comprehensive assertions

### Object Repository Management
- Use meaningful object names
- Implement robust locator strategies
- Maintain object hierarchy
- Regular object health checks

### Maintenance
- Update object locators when app changes
- Review and update test data regularly
- Monitor test execution reports
- Keep dependencies updated

## 🔧 Troubleshooting

### Common Issues
1. **Appium Connection Failed**
   - Verify Appium server is running
   - Check device connection
   - Validate desired capabilities

2. **Object Not Found**
   - Update object locators
   - Check app version compatibility
   - Verify screen orientation

3. **Test Data Issues**
   - Validate input data format
   - Check character encoding
   - Verify date formats

## 📞 Support

For technical support or questions:
- Review Katalon Studio documentation
- Check Appium troubleshooting guides
- Consult mobile testing best practices

---

**Last Updated**: January 2024  
**Katalon Studio Version**: Compatible with latest versions  
**Target Platform**: Android Mobile Applications
