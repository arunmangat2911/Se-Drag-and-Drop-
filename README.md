# Se-Drag-and-Drop-

package SeleniumSession;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;

public class DragAndDrop {

	public static void main(String[] args) {
			
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\Arun\\eclipse-workspace\\Selenium\\lib\\chromedrivers\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		
		driver.manage().window().maximize();
		
		driver.get("http://jqueryui.com/droppable/");
		
		driver.switchTo().frame(0);
		
		Actions action = new Actions(driver);
		
		action.clickAndHold(driver.findElement(By.xpath("//*[@id=\"draggable\"]")))
		.moveToElement(driver.findElement(By.xpath("//*[@id=\"droppable\"]")))
		.release()
		.build()
		.perform();
		
		

		

	}

}
