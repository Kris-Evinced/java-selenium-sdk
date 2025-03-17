# java-selenium-sdk

setup selenium sdk
First cloned Max Dobeck's repo: https://github.com/max-evinced/java-selenium-evinced

### SDK Debug Logging Configuration Example
```
EvincedConfiguration evincedConfiguration = new EvincedConfiguration();
EvincedWebDriver evincedDriver = new EvincedWebDriver(driver, evincedConfiguration);
configuration.setLoggingConfiguration(LoggingConfiguration.builder()
        .loggingEnabled(true) // mandatory - enables/disables logging. Overrides the environment variable, if set.
        .loggingLevel("debug") // mandatory - sets the general logging level.
        .logsFolder("target/logs/evinced") // mandatory - updates the logging folder
        .browserLoggingEnabled(false) // optional - enables gathering log from browser console. Requires additional chrome capability. Covered below in the page.
        .systemInformationLoggingEnabled(true) // mandatory -enables logging of system information: SDK versions, OS name, version, Java version, Java VM version
        .maxLogLength(1000) // optional - Updates the max length of written log messages, defaults to 1000.
        .build()); 
EvincedWebDriver driver = new EvincedWebDriver(new ChromeDriver(), evincedConfiguration);
```
