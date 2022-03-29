# Absa_assessment
# Absa Assessment
This is a automation testing project for http://www.way2automation.com/angularjs-protractor/webtables/. This project is build using Java, IntelliJ IDE, Maven and Selenium WebDriver. The automation testing covers the scenario:
Navigate to http://www.way2automation.com/angularjs-protractor/webtables/
Validate that you are on the User List Tabllogin account,
Click Add user, Ensure that User Name (*) is unique on each run
Ensure that your users are added to the list

##General Usage Guide
This project requires IntelliJ IDE or similar IDE and Chrome Browser.

Clone the Absa_assessment repository by
    git clone https://github.com/Xolisa213000152/Absa_assessment.git
	file is zip folder make sure you on the right folder when opening it
Import project absa_assessment into IntelliJ IDE.
Open IntelliJ IDE. Probably you could also use Eclipse IDE, similar process to import maven project.
Select "Import Project".
Go to the project directory and Choose folder "Absa_assessment".
Select "Import project from external model" and then select "Maven".
Checkout "Import Maven project automatically" and select "Next".
Select "Next" and then "Finish".
Compile project ocdes
In header bar, click "Build" and then select "Make Project".
Run automation testing
In header bar, click "Run" and then select "Run..."

Project Background

This is an automation project that navigates user to : http://www.way2automation.com/angularjs-protractor/webtables/ 
 > First it validates if user is on the correct user table using the created method : 
 > It will the add first user using the methods created on Add_New_User_To_User_Table class
 > Next step is verifying that the first user was added correctly using method : Verify_Added_User
  >>To verify if user is added correctly I use the Excel data sheet to read first line and user the firstname and lastname to verify if there we added
  
 >Secondly it adds the second user from Excel name DataSheet same steps as above only difference is that it is reading the second row
 

Functionality:
------------------------------------------------------
Unique UserName : I created a method below that will user half of the username from excel and current datetime to ensure username is always unique

  /*public void Add_UserName(String un) {
        WebDriverWait wait_for_username = new WebDriverWait(driver, 10);
        wait_for_username.until(ExpectedConditions.visibilityOf(UserName));
        Runtime.Timestamp timestamp = new Runtime.Timestamp(System.currentTimeMillis());
        un+="_"+timestamp;
        UserName.clear();
        UserName.sendKeys(un);*/
-----------------------------------------------------
.Clear()
I user variable/element.clear() as show below to ensure that before we send anything to that field that the field is empty

 UserName.clear();
 
-----------------------------------------------------

