package automation;

import java.util.List;

import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class Flipkart {

	public static void main(String[] args) throws InterruptedException {
System.setProperty("webdriver.chrome.driver", "D:\\chromedriver\\chromedriver.exe");
WebDriver d=new ChromeDriver();
d.manage().window().maximize();
d.get("https://www.flipkart.com");
d.findElement(By.xpath("//input[@type=\"Username\"]")).sendKeys("  USER NAME");
d.findElement(By.xpath("//input[@type=\"password\"]")).sendKeys(" PASSWORD");
d.findElement(By.xpath("//div[@class='O8ZS_U']/input")).sendKeys("Iphone");
d.findElement(By.xpath("//div[@class='O8ZS_U']/input")).sendKeys(Keys.ENTER);
Thread.sleep(5000);
d.findElement(By.xpath("//li[text()='Price -- Low to High']")).click();

Thread.sleep(5000);
List<WebElement> element =  d.findElements(By.xpath("//div[@class='_1vC4OE _2rQ-NK']"));

element.get(0).click();
	}
}
