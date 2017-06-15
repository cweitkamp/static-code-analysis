# Static Code Analysis Tool

The Static Code Analysis Tools is a Maven plugin that executes the Maven plugins for FindBugs, Checkstyle and PMD and generates a merged .html report.
It is specifically designed for Eclipse SmartHome and openHAB code as it is tailored to respect their coding guidelines.

This project contains:

 - properties files for the PMD, Checkstyle and FindBugs Maven plugins configuration in the `src/main/resources/configuration` folder;
 - rule sets for the plugins in the `src/main/resources/rulesets` folder;
 - custom rules for PMD, CheckStyle and FindBugs and unit tests for the rules;
 - tool that merges the reports from the individual plugins in a summary report.

## Essentials

1. [A list of included checks.](docs/included-checks.md)
2. [How to use and configure the Static Analysis Tool.](docs/maven-plugin.md)
3. [How to integrate a new check into the tool.](docs/implement-check.md)

## 3rd Party

- The example checks provided in the `static-code-analysis-config` (`MethodLimitCheck`, `CustomClassNameLengthDetector`, `WhileLoopsMustUseBracesRule`) are based on tutorials how to use the API of Checkstyle, FindBugs and PMD. For more info, see javadoc;
- The tool that merges the individual reports is based completely on source files from the https://github.com/MarkusSprunck/static-code-analysis-report that are distributed under a custom license. More information can be found in the [LICENSE](LICENSE) file.
