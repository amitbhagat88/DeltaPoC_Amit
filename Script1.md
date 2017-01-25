# Script1

public class SingleTest extends BrowserStackTestNGTest {

    @Test
    public void test() throws Exception {
        driver.get("https:// www.delta.com/");
        WebElement element = driver.findElement(By.name("originCity"));
        element.sendKeys("SFO");
        WebElement element = driver.findElement(By.name("destinationCity"));
        element.sendKeys("BOM");

        element.submit();
        Thread.sleep(5000);

        Assert.assertEquals("From SFO to BOM – Find Flights", driver.getTitle());
    }
}
