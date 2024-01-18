java
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class WebScraper {
    public static void main(String[] args) {
        // Set the path of the chrome driver executable
        System.setProperty("webdriver.chrome.driver", "/path/to/chromedriver");

        // Initialize ChromeDriver and navigate to desired URL
        WebDriver driver = new ChromeDriver();
        driver.get("https://www.example.com");

        // Find element(s) using By.id() and print text content
        WebElement elementById = driver.findElement(By.id("example-id"));
        System.out.println(elementById.getText());

        // Find element(s) using By.name() and print text content of first result only
        WebElement elementByName = driver.findElements(By.name("example-name")).get(0);
        System.out.println(elementByName.getText());

        // Close the browser session
        driver.quit();
    }
}# Portfolio