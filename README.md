# **Gauge Framework'ü ile Web Test Otomasyonu**
# Hepsiburada Web Scenario
# AllSteps Web Login Scenario
**Tags:chrome**
1. [x] **Login bilgileri girilir.**
2. [x] **Anasayfaya kullanıcı giriş işlemi yaptığı doğrulanır.**
3. [x] **Tercih edilen ürün için arama yapılır.**
4. [x] **Arama yapılan ürün ile Yeni Sekmede işleme devam edilir.**
5. [x] **Ürün ilk açılan satıcıdan sepete eklenir.**
6. [x] **Farklı satıcıdan ürün tekrardan sepete eklenir.**
7. [x] **Sepete gidilir, doğru ürünlerin seçildiği ve sepete eklendiği doğrulanır.**

# AllSteps Web Non-Login Scenario
**Tags:chrome**
1. [x] **Çerezler kabul edilir.**
2. [x] **Tercih edilen ürün için arama yapılır.**
3. [x] **Arama yapılan ürün ile Yeni Sekmede işleme devam edilir.**
4. [x] **Ürün ilk açılan satıcıdan sepete eklenir.**
5. [x] **Farklı satıcıdan ürün tekrardan sepete eklenir.**
6. [x] **Sepete gidilir, doğru ürünlerin seçildiği ve sepete eklendiği doğrulanır.**

 ```
  
  <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <java.version>1.8</java.version>
        <gauge.version>0.9.1</gauge.version>
        <selenium.version>3.141.59</selenium.version>
        <gauge.plugin.version>1.3.4</gauge.plugin.version>
        <maven.compiler.version>3.7.0</maven.compiler.version>
        <log4j.version>1.7.30</log4j.version>
        <gson.version>2.8.8</gson.version>
        <bonigarcia.version>5.2.2</bonigarcia.version>
    </properties>

    <dependencies>
        <dependency>
            <groupId>com.thoughtworks.gauge</groupId>
            <artifactId>gauge-java</artifactId>
            <version>${gauge.version}</version>
            <scope>test</scope>
            <exclusions>
                <exclusion>
                    <groupId>com.google.guava</groupId>
                    <artifactId>guava</artifactId>
                </exclusion>
            </exclusions>
        </dependency>
        <dependency>
            <groupId>org.junit.jupiter</groupId>
            <artifactId>junit-jupiter-engine</artifactId>
            <version>5.1.0</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.seleniumhq.selenium</groupId>
            <artifactId>selenium-java</artifactId>
            <version>${selenium.version}</version>
            <scope>test</scope>
        </dependency>
        <!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->
        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <version>8.0.21</version>
        </dependency>
        <dependency>
            <groupId>io.github.bonigarcia</groupId>
            <artifactId>webdrivermanager</artifactId>
            <version>${bonigarcia.version}</version>
        </dependency>
        <dependency>
            <groupId>com.microsoft.sqlserver</groupId>
            <artifactId>mssql-jdbc</artifactId>
            <version>8.2.2.jre11</version>
        </dependency>
        <dependency>
            <groupId>org.slf4j</groupId>
            <artifactId>slf4j-log4j12</artifactId>
            <version>${log4j.version}</version>
        </dependency>
        <dependency>
            <groupId>org.slf4j</groupId>
            <artifactId>slf4j-api</artifactId>
            <version>${log4j.version}</version>
        </dependency>
        <dependency>
            <groupId>com.google.code.gson</groupId>
            <artifactId>gson</artifactId>
            <version>${gson.version}</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <version>1.18.24</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>com.fasterxml.jackson.core</groupId>
            <artifactId>jackson-databind</artifactId>
            <version>2.13.3</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.13.2</version>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>io.appium</groupId>
            <artifactId>java-client</artifactId>
            <version>7.3.0</version>
        </dependency>

    </dependencies>

    <build>
        <testResources>
            <testResource>
                <directory>src/test/resources</directory>
            </testResource>
        </testResources>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>${maven.compiler.version}</version>
                <configuration>
                    <source>${java.version}</source>
                    <target>${java.version}</target>
                </configuration>
            </plugin>
            <plugin>
                <groupId>com.thoughtworks.gauge.maven</groupId>
                <artifactId>gauge-maven-plugin</artifactId>
                <version>${gauge.plugin.version}</version>
            </plugin>
        </plugins>
    </build>

 ```