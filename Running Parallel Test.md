# parallel.conf.json
{
  "server": "hub-cloud.browserstack.com",
  "user": "amitbhagat2",
  "key": "qyCnopYAB8yE1ELXpiG8",

  "capabilities": {
    "browserstack.debug": true
  },

  "environments": {
    "chrome": {
      "browser": "chrome 54"
    },
    "firefox": {
      "browser": "firefox 48"
    },
    "safari": {
      "browser": "safari"
    },
    "ie": {
      "browser": " IE 11 "
    }
  }
}

# parallel.testng.xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE suite SYSTEM "http://testng.org/testng-1.0.dtd">
<suite name="Parallel" thread-count="4" parallel="tests">
    <test name="SingleTestChrome">
        <parameter name="config" value="parallel.conf.json"/>
        <parameter name="environment" value="chrome"/>
        <classes>
            <class name="com.browserstack.SingleTest"/>
        </classes>
    </test>

    <test name="SingleTestFirefox">
        <parameter name="config" value="parallel.conf.json"/>
        <parameter name="environment" value="firefox"/>
        <classes>
            <class name="com.browserstack.SingleTest"/>
        </classes>
    </test>

    <test name="SingleTestIE">
        <parameter name="config" value="parallel.conf.json"/>
        <parameter name="environment" value="ie"/>
        <classes>
            <class name="com.browserstack.SingleTest"/>
        </classes>
    </test>
</suite>
