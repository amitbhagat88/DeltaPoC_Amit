// single.conf.json
{
  "server": "hub-cloud.browserstack.com",
  "user": "amitbhagat2",
  "key": "qyCnopYAB8yE1ELXpiG8",

  "capabilities": {
    "browserstack.debug": true
  },

  "environments": {
    "chrome": {
      "browser": "chrome"
    }
  }
}

// single.testng.xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE suite SYSTEM "http://testng.org/testng-1.0.dtd">
<suite name="Single">
    <test name="SingleTest">
        <parameter name="config" value="single.conf.json"/>
        <parameter name="environment" value="chrome"/>
        <classes>
            <class name="com.browserstack.SingleTest"/>
        </classes>
    </test>
</suite>
