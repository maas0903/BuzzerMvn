# BuzzerMvn

Java Maven project for active and passive buzzer for Raspberry Pi

#### The harware pwm must be run with sudo:
1.Add this to pom.xml:

    <build> 
        <plugins>
            <plugin>
                <groupId>org.rogueware.mojo</groupId>
                <artifactId>ssh-exec-maven-plugin</artifactId>
                <version>1.2</version>
                <configuration>
                    <sshHost>192.168.63.24</sshHost>
                    <sshUsername>pi</sshUsername>
                    <sshPassword>raspberry</sshPassword>
                    <sudo>true</sudo>
                    <sudoPassword>raspberry</sudoPassword>
                </configuration>
            </plugin>
        </plugins>
    </build>
	
2.Program properties:
Actions/Run project - Execute Goals: process-classes org.rogueware.mojo:ssh-exec-maven-plugin:1.2:exec
Actions/Debug project - process-classes org.rogueware.mojo:ssh-exec-maven-plugin:1.2:exec
