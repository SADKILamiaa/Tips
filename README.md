# Tips 

   1/ Couldn’t PUSH my remote repositories from the command line, the command line threw this error ==> "Authentication Failed from the Command Line"
        
        Solution : 
              Go to Settings ==> Developer Settings ==> Personal access token ==> Generate a new Personal Access Token ==> Paste the Personal Access Token into the           “Password”
              
        Source :  https://ginnyfahs.medium.com/github-error-authentication-failed-from-command-line-3a545bfd0ca8 
                  https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
           
   2/ dst root ca x3 expiration  ==> "Internet access on your Mac break on 30th September 2021"
    
        Solution : https://www.youtube.com/watch?v=WLG6XVZPF34
        
   3/ convertir votre projet en Maven et créer un pom.xml ==> clic droit sur le projet, sélectionnez Configurer → Convertir en projet Maven.
   
   4/ Error creating bean with name 'entityManagerFactory' defined in class path resource : Invocation of init method failed
         
         ==> 
                   <dependency>
                      <groupId>org.hibernate</groupId>
                      <artifactId>hibernate-core</artifactId>
                      <version>4.1.4.Final</version>
                   </dependency>
             and
                  <dependency>
                      <groupId>org.hibernate</groupId>
                      <artifactId>hibernate-entitymanager</artifactId>
                      <version>5.2.3.Final</version>
                  </dependency>
             OR
                  <dependency>
                      <groupId>javax.xml.bind</groupId>
                      <artifactId>jaxb-api</artifactId>
                      <version>2.3.0</version>
                  </dependency>
                  
                  
                  
   5/ The resource could not be loaded because the App Transport Security policy requires the use of a secure connection
            
            ==> Opened my Project target's info.plist file  
                  <key>NSAppTransportSecurity</key>
                      <dict>
                          <key>NSAllowsArbitraryLoads</key>
                          <true/>
                          <key>NSExceptionDomains</key>
                          <dict>
                              <key>yourdomain.com</key>
                              <dict>
                                  <key>NSIncludesSubdomains</key>
                                  <true/>
                                  <key>NSThirdPartyExceptionRequiresForwardSecrecy</key>
                                  <false/>
                              </dict>
                         </dict>
                    </dict>
        

   6/ Comment définir ou modifier la version par défaut de Java (JDK) sous OS X
   
      * Pour savoir les jdk présent sur votre PC ==> /usr/libexec/java_home -V 
      * Choisissez la version que vous souhaitez ==>  export JAVA_HOME=$(/usr/libexec/java_home -v 1.8)
         
         Source: https://qastack.fr/programming/21964709/how-to-set-or-change-the-default-java-jdk-version-on-os-x
               
               
        
    
    
    
    
