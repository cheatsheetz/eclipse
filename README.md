# Eclipse IDE Cheat Sheet

## Installation and Setup

### Installation Options
```bash
# Ubuntu/Debian
sudo snap install eclipse --classic

# macOS
brew install --cask eclipse-java

# Windows
winget install EclipseFoundation.EclipseIDE

# Manual Installation
# Download from https://www.eclipse.org/downloads/
# Extract and run eclipse executable
```

### Eclipse Installer
```text
Package Options:
- Eclipse IDE for Java Developers
- Eclipse IDE for Enterprise Java and Web Developers
- Eclipse IDE for C/C++ Developers
- Eclipse IDE for PHP Developers
- Eclipse IDE for Web and JavaScript Developers
- Eclipse IDE for Java and DSL Developers
- Eclipse IDE for Modeling Tools
- Eclipse IDE for Parallel Application Developers
```

### First Launch Setup
```text
1. Choose workspace directory
2. Install additional packages if needed
3. Configure JRE/JDK (Window → Preferences → Java → Installed JREs)
4. Set up Maven (if using Maven projects)
5. Configure Git settings
```

## Essential Keyboard Shortcuts

### General Navigation
| Shortcut | Action |
|----------|---------|
| `Ctrl+Shift+R` | Open Resource (File) |
| `Ctrl+Shift+T` | Open Type (Class) |
| `Ctrl+H` | Search |
| `Ctrl+Shift+G` | Search References |
| `Ctrl+Shift+H` | Search Call Hierarchy |
| `Ctrl+E` | Quick Switch Editor |
| `Ctrl+F6` | Next Editor |
| `Ctrl+Shift+F6` | Previous Editor |
| `Ctrl+M` | Maximize/Restore Editor |
| `F3` | Open Declaration |
| `F4` | Open Type Hierarchy |

### File Operations
| Shortcut | Action |
|----------|---------|
| `Ctrl+N` | New |
| `Ctrl+O` | Open |
| `Ctrl+S` | Save |
| `Ctrl+Shift+S` | Save All |
| `Ctrl+W` | Close |
| `Ctrl+Shift+W` | Close All |
| `Ctrl+F4` | Close Editor |
| `Alt+Enter` | Properties |

### Editing
| Shortcut | Action |
|----------|---------|
| `Ctrl+Space` | Content Assist |
| `Ctrl+Shift+Space` | Context Information |
| `Alt+/` | Word Completion |
| `Ctrl+D` | Delete Line |
| `Ctrl+Shift+Enter` | Insert Line Above |
| `Shift+Enter` | Insert Line Below |
| `Alt+Up/Down` | Move Lines |
| `Ctrl+Alt+Up/Down` | Duplicate Lines |
| `Ctrl+Shift+Y` | Convert to Lowercase |
| `Ctrl+Shift+X` | Convert to Uppercase |
| `Tab` | Indent |
| `Shift+Tab` | Unindent |

### Code Navigation
| Shortcut | Action |
|----------|---------|
| `Ctrl+Shift+Up/Down` | Jump to Previous/Next Member |
| `Ctrl+L` | Go to Line |
| `Ctrl+Q` | Go to Last Edit Location |
| `Alt+Left/Right` | Go Back/Forward in History |
| `Ctrl+Shift+P` | Go to Matching Bracket |
| `Ctrl+T` | Quick Type Hierarchy |
| `Ctrl+Shift+T` | Open Type |
| `Ctrl+Shift+R` | Open Resource |

### Refactoring
| Shortcut | Action |
|----------|---------|
| `F2` | Rename |
| `Alt+Shift+R` | Rename (alternative) |
| `Alt+Shift+V` | Move |
| `Alt+Shift+C` | Change Method Signature |
| `Alt+Shift+M` | Extract Method |
| `Alt+Shift+L` | Extract Local Variable |
| `Alt+Shift+I` | Inline |
| `Alt+Shift+T` | Refactor Menu |
| `Ctrl+2` | Quick Assist |

### Search and Replace
| Shortcut | Action |
|----------|---------|
| `Ctrl+F` | Find/Replace |
| `F3` | Find Next |
| `Shift+F3` | Find Previous |
| `Ctrl+K` | Find Next Selected Text |
| `Ctrl+Shift+K` | Find Previous Selected Text |
| `Ctrl+H` | Search Dialog |
| `Ctrl+Shift+G` | Search References |

### Running and Debugging
| Shortcut | Action |
|----------|---------|
| `Ctrl+F11` | Run Last Launched |
| `F11` | Debug Last Launched |
| `Ctrl+Shift+F11` | Run |
| `Ctrl+Shift+D` | Debug |
| `F5` | Step Into |
| `F6` | Step Over |
| `F7` | Step Return |
| `F8` | Resume |
| `Ctrl+F2` | Terminate |
| `Ctrl+Shift+B` | Toggle Breakpoint |
| `Ctrl+Shift+I` | Inspect |

## Project Management

### Project Types
```text
Java Projects:
- Java Project (standard)
- Dynamic Web Project (servlets, JSP)
- Maven Project
- Gradle Project

Other Languages:
- C/C++ Project
- PHP Project  
- Python Project (with PyDev)
- JavaScript Project
```

### Project Structure
```text
Java Project Structure:
project-root/
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   └── test/
│       ├── java/
│       └── resources/
├── target/ (Maven)
├── bin/ (Eclipse compiled classes)
├── .classpath
├── .project
└── .settings/
```

### Workspace Management
```text
Workspace Organization:
- Use Working Sets to group related projects
- Create multiple workspaces for different contexts
- Import/Export workspace settings
- Use Project References for dependencies

Workspace Settings:
- Window → Preferences for global settings
- Right-click project → Properties for project-specific settings
```

## Java Development

### Code Generation
```text
Source Menu (Alt+Shift+S):
- Generate Getters and Setters
- Generate Constructors
- Generate hashCode() and equals()
- Generate toString()
- Override/Implement Methods
- Generate Delegate Methods
```

### Code Templates
```java
// Common Eclipse templates
sysout   → System.out.println();
syserr   → System.err.println();
for      → for (int i = 0; i < array.length; i++) {}
foreach  → for (Type item : collection) {}
while    → while (condition) {}
try      → try-catch block
test     → @Test public void testMethod() {}

// Custom template creation:
// Window → Preferences → Java → Editor → Templates
```

### Quick Fixes and Assists
```text
Common Quick Fixes (Ctrl+1):
- Import missing classes
- Create missing methods/fields
- Add unimplemented methods
- Surround with try-catch
- Convert to enhanced for loop
- Add @Override annotation
- Extract to method/variable

Quick Assists (Ctrl+2):
- Extract local variable (L)
- Rename in file (R)
- Assign to field (F)
- Generate getter/setter (G)
```

### Code Formatting
```text
Formatter Configuration:
Window → Preferences → Java → Code Style → Formatter

Key Settings:
- Indentation (tabs vs spaces)
- Line length (typically 80 or 120)
- Brace placement
- Blank line preferences
- Comment formatting

Apply Formatting:
- Ctrl+Shift+F: Format entire file
- Ctrl+Shift+F: Format selection
- Format on save: Preferences → Java → Editor → Save Actions
```

## Build Tools Integration

### Maven Integration (m2e)
```xml
<!-- pom.xml example -->
<project xmlns="http://maven.apache.org/POM/4.0.0">
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.example</groupId>
    <artifactId>my-app</artifactId>
    <version>1.0.0</version>
    
    <properties>
        <maven.compiler.source>11</maven.compiler.source>
        <maven.compiler.target>11</maven.compiler.target>
    </properties>
    
    <dependencies>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.13.2</version>
            <scope>test</scope>
        </dependency>
    </dependencies>
</project>
```

### Maven Operations
```text
Right-click project → Maven:
- Reload Projects
- Update Project
- Generate Sources and Update Folders
- Run As → Maven build
- Run As → Maven install
- Run As → Maven test

Maven Console:
- Window → Show View → Console
- Select Maven console for build output
```

### Gradle Integration (Buildship)
```gradle
// build.gradle example
plugins {
    id 'java'
    id 'eclipse'
}

repositories {
    mavenCentral()
}

dependencies {
    implementation 'org.springframework:spring-core:5.3.21'
    testImplementation 'junit:junit:4.13.2'
}

java {
    sourceCompatibility = JavaVersion.VERSION_11
    targetCompatibility = JavaVersion.VERSION_11
}
```

## Debugging

### Debug Configuration
```text
Run → Debug Configurations:
- Create new Java Application
- Set Main class
- Configure Program arguments
- Set VM arguments
- Environment variables
- Classpath settings
- Source lookup paths
```

### Debug Views
```text
Essential Debug Views:
- Debug: Shows call stack and thread information
- Variables: Shows variable values and object inspection
- Breakpoints: Manage all breakpoints
- Expressions: Watch expressions
- Console: Program output and error streams
```

### Advanced Debugging
```text
Breakpoint Types:
- Line breakpoints (standard)
- Method breakpoints
- Exception breakpoints
- Conditional breakpoints
- Hit count breakpoints

Debugging Features:
- Hot code replacement
- Drop to frame
- Step filtering
- Logical structures
- Variable inspection
- Memory view
```

## Version Control

### Git Integration (EGit)
```text
Git Operations:
- Team → Share Project (initialize repository)
- Team → Commit (stage and commit changes)
- Team → Push Branch (push to remote)
- Team → Pull (fetch and merge)
- Team → Switch To → Branch (change branches)

Git Views:
- Git Repositories: Repository overview
- Git Staging: Stage changes for commit
- History: View commit history
- Blame: Show file annotations
```

### Git Configuration
```text
Window → Preferences → Team → Git:
- Configuration: Set user name and email
- Cloning: Default clone directory
- Repositories: Repository locations
- Label Decorations: File status indicators

Repository Setup:
1. File → Import → Git → Projects from Git
2. Clone URI or Local repository
3. Select branches to clone
4. Choose import method
```

## Plugin Ecosystem

### Essential Plugins

#### Development Tools
```text
Language Support:
- PyDev (Python)
- CDT (C/C++)
- PDT (PHP) 
- JSDT (JavaScript)
- Wild Web Developer (modern web)

Build Tools:
- M2E (Maven)
- Buildship (Gradle)
- Ant

Version Control:
- EGit (Git)
- Subversive (SVN)
```

#### Code Quality
```text
- SpotBugs (static analysis)
- Checkstyle (code style)
- PMD (code analysis)
- SonarLint (continuous inspection)
- EclEmma (code coverage)
```

#### Productivity
```text
- Enhanced Class Decompiler
- Eclipse Color Theme
- AnyEdit Tools
- More Unit (test generation)
- Bracketeer (bracket matching)
- Quick Search (fast file search)
```

### Plugin Installation
```text
Eclipse Marketplace:
1. Help → Eclipse Marketplace
2. Search for plugin
3. Install and restart

Update Sites:
1. Help → Install New Software
2. Add update site URL
3. Select features to install
4. Complete installation wizard

Popular Update Sites:
- Eclipse Marketplace: http://marketplace.eclipse.org
- Spring Tools: https://spring.io/tools
- JBoss Tools: http://download.jboss.org/jbosstools/
```

## Customization

### Workspace Preferences
```text
Key Preference Categories:
- General → Appearance (theme, colors, fonts)
- General → Editors (editor behavior, associations)
- Java → Appearance (syntax coloring, member sort)
- Java → Code Style (formatting, cleanup)
- Java → Compiler (compliance level, warnings)
- Java → Debug (debugging preferences)
- Team → Git (version control settings)
```

### Key Bindings
```text
Customize Shortcuts:
1. Window → Preferences → General → Keys
2. Search for command
3. Set new key binding
4. Resolve conflicts
5. Apply and test

Scheme Options:
- Default
- Emacs  
- Microsoft Visual Studio
- WordStar
```

### Perspectives
```text
Built-in Perspectives:
- Java (default Java development)
- Debug (debugging layout)
- Git (version control)
- Team Synchronizing (file comparison)

Custom Perspectives:
1. Arrange views and editors as desired
2. Window → Perspective → Save Perspective As
3. Name and save custom layout
4. Switch between perspectives as needed
```

## Performance Optimization

### Memory Settings
```text
eclipse.ini Configuration:
-vmargs
-Xms512m          # Initial heap size
-Xmx2g            # Maximum heap size
-XX:MaxPermSize=256m  # Permanent generation (Java 7 and earlier)
-XX:MaxMetaspaceSize=512m  # Metaspace (Java 8+)

Recommended for large projects:
-Xms1g
-Xmx4g
-XX:MaxMetaspaceSize=1g
```

### Performance Tips
```text
Workspace Optimization:
- Close unused projects
- Disable automatic building for large projects
- Exclude irrelevant directories from build path
- Use working sets to organize projects
- Limit text file encoding detection

Build Optimization:
- Enable parallel builds (Preferences → General → Workspace)
- Increase build job limit
- Use incremental builders
- Configure build scope appropriately
```

## Troubleshooting

### Common Issues
```text
Workspace Corruption:
1. Close Eclipse
2. Delete .metadata\.plugins\org.eclipse.core.resources\.projects\<project>\.location
3. Reimport project
4. Or create new workspace and import projects

Build Path Issues:
1. Right-click project → Properties → Java Build Path
2. Check Source folders
3. Verify Library dependencies
4. Update Project (if Maven/Gradle)

Out of Memory:
1. Increase heap size in eclipse.ini
2. Close unused projects
3. Clear workspace cache
4. Restart with -clean flag
```

### Debug and Logging
```text
Error Log:
Window → Show View → Error Log

Eclipse Console:
- Shows application output
- Switch between different consoles
- Configure console buffer size

Workspace Logs:
Location: <workspace>/.metadata/.log
- Contains detailed error information
- Useful for plugin issues
- Include in bug reports
```

## Testing

### JUnit Integration
```java
// JUnit 4 test example
import org.junit.Test;
import org.junit.Assert;

public class CalculatorTest {
    @Test
    public void testAddition() {
        Calculator calc = new Calculator();
        int result = calc.add(2, 3);
        Assert.assertEquals(5, result);
    }
}

// JUnit 5 test example  
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

class CalculatorTest {
    @Test
    void testAddition() {
        Calculator calc = new Calculator();
        int result = calc.add(2, 3);
        assertEquals(5, result);
    }
}
```

### Test Runners
```text
Running Tests:
- Right-click test → Run As → JUnit Test
- Run All Tests in package/project
- Debug tests with debugger
- View test results in JUnit view

Test Generation:
- Right-click class → New → JUnit Test Case
- Generate test methods for existing methods
- Use templates for common test patterns
```

## Web Development

### Dynamic Web Projects
```text
Project Setup:
1. File → New → Dynamic Web Project
2. Configure target runtime (Tomcat, etc.)
3. Set up project structure
4. Configure deployment assembly

Project Structure:
WebContent/
├── META-INF/
├── WEB-INF/
│   ├── lib/
│   └── web.xml
├── css/
├── js/
├── images/
└── index.jsp
```

### Server Integration
```text
Supported Servers:
- Apache Tomcat
- JBoss/WildFly
- WebLogic
- WebSphere
- Jetty

Server Configuration:
1. Window → Show View → Servers
2. Right-click → New → Server
3. Choose server type and version
4. Configure server runtime
5. Deploy projects to server
```

## Best Practices

### Project Organization
```text
Code Organization:
- Use meaningful package names
- Follow Java naming conventions
- Separate source and test code
- Use appropriate access modifiers
- Document public APIs

Workspace Management:
- Use consistent workspace layout
- Create project templates
- Use working sets for project grouping
- Regular workspace cleanup
- Backup workspace settings
```

### Code Quality
```text
Quality Practices:
- Enable compiler warnings
- Use code formatters consistently
- Run static analysis tools
- Write comprehensive tests
- Use version control effectively
- Regular code reviews
```

## Official Documentation

- [Eclipse Documentation](https://www.eclipse.org/documentation/)
- [Eclipse IDE User Guide](https://help.eclipse.org/latest/index.jsp)
- [Eclipse Platform Plug-in Developer Guide](https://help.eclipse.org/latest/index.jsp?topic=%2Forg.eclipse.platform.doc.isv%2Fguide%2Findex.html)
- [Eclipse Marketplace](https://marketplace.eclipse.org/)
- [Eclipse Community Forums](https://www.eclipse.org/forums/)
- [Eclipse Bugzilla](https://bugs.eclipse.org/bugs/)
- [Eclipse Foundation](https://www.eclipse.org/org/)
- [Eclipse IDE FAQ](https://wiki.eclipse.org/Eclipse_IDE_FAQ)