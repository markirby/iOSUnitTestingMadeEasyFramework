# iOS Unit Testing Made Easy

## Introduction

This project is born out of my frustrations with limited documentation, advice and support for unit testing iPhone apps.

This will be a defined method of unit testing iOS applications through a combination of templates, protocols and helpers. 

At the moment this is just a work in progress, I'll announce soon when its ready.

## Installing for Xcode 4

To install the library you can follow the method as described by Jonah Williams in his excellent article [Using Open Source Static Libraries in Xcode 4](http://blog.carbonfive.com/2011/04/04/using-open-source-static-libraries-in-xcode-4/) which tells us to do the following.

### Download the project

Download the entire git repos into a folder somewhere, I'll refer to the folder this creates as {iOSUnitTestingMadeEasyFramework/}

I'll refer to the project you are adding this to as {MainProject}

### Create a workspace (if you aren't using one already)

1. Open the project you wish to add the framework to
2. File -> Save as workspace

### Add the iOS Unit Testing Made Easy framework

1. Right click on the project navigator (left hand column) -> Add files to {MainProject}
2. Navigate to {iOSUnitTestingMadeEasyFramework/iOSUnitTestingMadeEasyFramework.xcodeproj}
3. Uncheck copy items into destinations folder
4. Click Add

### Add build target dependencies

1. Select {MainProject} in the project navigator
2. Select {MainProject} in the Targets section of the second column from left.
3. Open the "Link Binary With Libraries" build phase
4. Click the +
5. Select the file iOSUnitTestingMadeEasyFramework.a
6. Click "Add"

The file iOSUnitTestingMadeEasyFramework.a should show up in the left hand column and it will be red, which is rather alarming but not to worry.

### Add the static libraries headers

1. Select {MainProject} in the project navigator
2. Select {MainProject} in the Targets section of the second column from left.
3. Select the "Build settings" tab
4. Search for "User Header Search Paths" 
5. Double click on the field
6. Check the "Recursive" icon
7. Enter "$(BUILT_PRODUCTS_DIR)"

### Configure the scheme

1. Go to the schema drop down "{MainProject} > iPhone 5.0 Simulator"
2. Select the "Build" tab
3. Click "+" and add the iOSUnitTestingMadeEasyFramework
4. Set it to the first framework
5. Ensure all checkboxes are checked

### Restart XCode!

### Add the header files

Drag all files in the protocol folder and headers folder in iOSUnitTestingMadeEasyFramework over into your project, DON'T add them to any targets.

