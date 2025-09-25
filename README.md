# Elevate-Labs-Internship--Task-3
Task 3
1.First install OpenVAS by entering the code "sudo apt-get install openvas" in terminal
2.After installing openvas we need to setup using "gvm-setup". this may take a minute because it creates unique userid,name and password
3.After the setup is done. note down the id and passwords in text file to remember. Now to we need to download the required feeds t orun the vulnerability assessment
4.Now enter into openvas location by turning into root user. Then to update enter these codes one by one after each is updated
  sudo runuser -u _gvm -- greenbone-nvt-sync
  sudo runuser -u _gvm -- greenbone-feed-sync --type SCAP
  sudo runuser -u _gvm -- greenbone-feed-sync --type CERT
  sudo runuser -u _gvm -- greenbone-feed-sync --type GVMD_DATA
These are nothing but the policies,vulnerability tests,CVe. etc
5. After every update is done, Now start openvas by enetering the commnad "gvm-start"
6.It will take few seconnds to open the website portal automatically. Then enter the username and password to login
7.Now go to the task section in category and add new task. then enter the required details.Enter your IP address and click save
8.Now start the test. This will take more time depending on your network and Pc performance.
9.After it completed, open the report and check the vulnerabilities(EG:For me its SSL/TLS: Report Weak Cipher Suites). 
10.MITIGATION:
              1.he configuration of this services should be changed so that it does not accept the listed weak cipher suites anymore
              2.Edit your service’s TLS configuration. Depending on what server you’re running (Apache, Nginx, OpenSSL-based service, etc.), you need to restrict cipher suites
11.Document the most critical Vulnerabilities.
12.I have added the screenshots of my vulnerability test
