# Basic Template



## Getting started

This project contains Automation test Scripts for {Project_name}

In order to perform following automation test scripts, we need to install few softwares: 

1. Java jdk-1.8 or higher 

	-> Link: https://www.oracle.com/in/java/technologies/downloads/

2. Integrated development environment (IDE)

	You can download either IntelliJ Idea IDE or Eclipse IDE.

	-> Link for IntelliJ: https://www.jetbrains.com/idea/

	-> Link for Eclipse: https://www.eclipse.org/downloads/

	If Eclipse is chosen, 

	Open the IDE and download Cucumber and TestNG Plugins from Help -> Eclipse Marketplace

3. Different browsers need to be installed (if cross-browser is performed).

	On a safer side, chrome, firefox, and edge can be installed. 

To open the automation framework, following two ways can be followed:

- Clone the project repository and import it in the IDE. Or
- Download the Zip file and set it up in your local workspace.

## Introduction to Framework

This Test Automation Framework is created using Java + Selenium Web Driver + TestNG + Cucumber. Which can be used across different web based applications. 
Additionally, it offers the ability to capture screenshots for tests and generate error shots for failed test cases.

In this repository, we encourage the use of Behavior-Driven Development (BDD) with Cucumber and Java to develop automation scripts. 
We provide predefined Step Definitions packaged under /Basic_Template/src/test/java/Stepdef/homeScreen.java to help you accelerate your automation development. 
These Step Definitions can be customized according to your needs.

Tests are written in the Cucumber framework using the Gherkin syntax. If you're new to Gherkin and Cucumber, you can find more information at https://cucumber.io/docs/cucumber/

A typical test will have a structure similar to this:

	Feature: Verify user redirection on web application
		Scenario: Verify USer is redirected to correct url
			Given Enter URL	
			When Browser is Open	
			Then User is redirected to URL
			


Automation test scripts are implemented with PAGE OBJECT MODEL (POM) design pattern.

To better organize the test code and make it more maintainable, it is recommended to use the Page Object Design Pattern. 
With this pattern, the UI elements of the web application are modeled as objects within the test code. This approach reduces code duplication and allows easy updates if the UI changes. 
The Page Object pattern provides a solution by centralizing selectors (classes, Xpaths, IDs, etc) in separate .java files, where we can manage them along with the associated methods. 

## Framework Structure

The automation framework structure is as follows:

- Under src/test/java, there are Page object classes, Test runner class, and Step definitions.
- Under src/test/resources, there are Feature files.
- Reports are generated in two folders: SwagLabs_Project\Reports and SwagLabs_Project\target\HTMlReports\report.html
- There is a POM.xml file in which all dependencies and plugins are there.
- There is also a testng.xml file located at SwagLabs_Project\testng.xml for cross browser testing.