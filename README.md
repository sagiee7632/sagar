# sagar
.	It is called a wild card character, It matches any one character other than the new line.
^	It matches the start of the string.
$	It matches the end of the string.
*	It matches up to zero or more occurrences i.e. any number of times of the character of the string.
\	It is used for escape following character.
()	It is used to match or search for a set of regular expressions.


# use 
fruits_file=`cat fruit.txt | grep App.e`

------------------------------------------------------------------------------------------------------------------------------------------
Step 1: Create a Java Project
(MY Java Project Name SumLargestNumberr.java)

Step 2:Create a Dockerfile in the same folder of your code with theabove details:

# Use the official OpenJDK image as the base
FROM openjdk:17-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the Java file to the container
COPY SumLargestNumberr.java .

# Compile the Java program
RUN javac SumLargestNumberr.java

# Run the Java program when the
container starts

ENTRYPOINT ["java","SumLargestNumberr"]



Step 3:Now change the Dockerfile.txt into Dockerfile by removing its extensions

-----------ren Dockerfile.txt Dockerfile


Step 4: Build an image

 --------------docker build -t my-java-app .

To check whether the image is created or not do
docker images

Step 5: Build an image

To only create and run the container

----------------docker run -d --name my-java-container my-java-app

Run the Container with Interactive
Mode

----------------docker run -it --name my-java-container my-java-app




**********************************************************************************************
GITHUB

THESE STEPS NEED TO BE EXECUTED IN THE CMD ON THE FOLDER YOU HAVE CTREATED
step 1 : git config --global user.name "username"
step 2 : git config --global user.email "email"
step 3 : git init
STEP 4 : git add .
step 5 : git status (TO CHECK THE STATUS)
step 6 : git commit -m "MESSAGE"
step 7 : git remote add origin URL OF REPOSITORY
step 8 : git push origin master

AFTER CHANGING THE FILE
STEP 1 : git add file_name
step 2 : git commit -m "MESSAGE"
step 3 : git push origin master

********************************************************************************************

WITH THE HELP OF TESTNG 

package com.cdac.act;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.annotations.Test;

public class AppTest{
	
//	public static void main(String[] args) {
	
	@Test(priority = 1)
	 public void enterData() { 
		WebDriver driver=new ChromeDriver();
		driver.get("https://accounts.google.com/v3/signin/identifier?continue=https%3A%2F%2Fmail.google.com%2Fmail%2F&ifkv=AeZLP9_5rNeCPBZAjy4G-0iiQ5ETagkW3YZI-hft1AdqycTh-_vKJN_NFT7E6Jp-XX8F5XnkQcN3kg&rip=1&sacu=1&service=mail&flowName=GlifWebSignIn&flowEntry=ServiceLogin&dsh=S-133987948%3A1734790728574653&ddm=1");
		
		WebElement search=driver.findElement(By.xpath("//*[@id=\"identifierId\"]"));
		
		search.sendKeys("skshdiya@gmail.com");
	    driver.findElement(By.xpath("//*[@id=\"identifierNext\"]/div/button")).click();
		
		
	}
	
}
