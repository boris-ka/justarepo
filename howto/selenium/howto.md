## Запуск Selenium WebDriver в связке с Firefox

WebDriver не поддерживает новую версию Firefox. Нужно его поменять на geckodriver.

Firefox 45 ESR должна нормально поддерживаться WebDriver-ом, который старый.

Firefox 45.9 ESR x86 нормально запустилась в связке с WebDriver версии 2.52.0

=== CUT HERE ===

    <groupId>my-projects</groupId>
    <artifactId>test-selenium</artifactId>
    <version>1.0-SNAPSHOT</version>

    <dependencies>
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>2.52.0</version>
        </dependency>
    </dependencies>

------ >8 ------

Информация о запуске Firefox для тестов через IDEA (взято из  ProcExp):

"C:\Program Files\Mozilla Firefox\firefox.exe" -marionette -foreground -no-remote -profile C:\Users\UserName\AppData\Local\Temp\rust_mozprofile.PPRpSrvIrkD5

Work dir: C:\WorkSpace\selenium\

