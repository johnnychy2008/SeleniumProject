# SeleniumProject
demo
package co.edureka.selenium.demo;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.SessionNotCreatedException;
import org.openqa.selenium.chrome.ChromeDriver;

public class demo {

	public static void main(String[] args) throws InterruptedException {
		
System.setProperty("webdriver.chrome.driver", "C:\\Users\\johns\\Downloads\\chromedriver_win32//chromedriver.exe");
WebDriver driver = new ChromeDriver();
driver.get("http://www.gmail.com/");
driver.manage().window().maximize();
driver.findElement(By.id("identifierId")).sendKeys("johnson.anya@gmail.com");
Thread.sleep(2000);
driver.findElement(By.className("CwaK9")).click();
Thread.sleep(2000);
String at = driver.getTitle();
String ex = "gmail";
driver.close();
if(at.equalsIgnoreCase(ex))
{
	System.out.println("Test Successful");
	
}
else
{
	System.out.println("Test Failure");
}
	}

}
