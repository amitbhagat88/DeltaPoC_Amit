# Script3

public class SingleTest extends BrowserStackTestNGTest {

    @Test
    public void test() throws Exception {
        driver.get("https:// www.delta.com/");
        WebElement element = driver.findElement(By.name("hotelLocation"));
         element.submit();
        Thread.sleep(5000);

        Assert.assertEquals("Flight Details", driver.getTitle());
    }
}
