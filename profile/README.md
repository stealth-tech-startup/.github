I believe continuous innovation is the strongest force that drives a team in the right direction, because it implements [iterative product discovery](https://www.amazon.com/INSPIRED-Create-Tech-Products-Customers/dp/1119387507). My definition of innovation is

<p align="center">
<b>An innovation is a prototyping that changes my life in 2 hours</b>
</p>

This org is dedicated for technologies that makes it happen

_Rapid_ Prototyping Tools
-------------------------

- [ConvnetJS](http://cs.stanford.edu/people/karpathy/convnetjs/demo/classify2d.html)
- [OpenStack Swift Docker Image](https://github.com/stealth-tech-startup/docker-swift-onlyone)
- [JWT Playground](https://jwt.io/)
- [Cloudcraft](https://www.cloudcraft.co/)
- [GraphQL server for fast prototyping](https://github.com/stealth-tech-startup/json-graphql-server)
- [(React) Authentication through Keycloak](https://github.com/stealth-tech-startup/react-keycloak-authentication)
- [Mockbin](https://github.com/stealth-tech-startup/mockbin)
- [Docker Registry UI](https://github.com/stealth-tech-startup/docker-registry-ui)
- [NPM Trends](https://github.com/stealth-tech-startup/npm-trends)
- [QuickChart](https://github.com/stealth-tech-startup/quickchart)

  - [Documentation](https://stealth-tech-startup.github.io/quickchart-docs/)

- [wekan](https://github.com/wekan/wekan): Open Source Kanban
- [NextCloud](https://nextcloud.com/)
- <details><summary>VirtualBox</summary>

  - Start VM from command line

    ```bash
    VBoxManage startvm <vm_name> --type headless
    ```

  - Stop virtual machine

    ```bash
    VBoxManage controlvm <vm_name> poweroff
    ```

  - [SSH into a virtual machine](https://www.cyberciti.biz/faq/ubuntu-linux-install-openssh-server/)
 
    1. To open guest machine network settings to make sure it's attached to NAT
   
       ![](https://averagelinuxuser.com/assets/images/posts/2022-05-21-ssh-into-virtualbox/Virtualbox-NAT.jpg)

    2. Then go to _Advanced_ -> **_Port Forwarding_** and add these settings:

       - The IP fields can be left empty.
       - Name: ssh (or whatever you like)
       - Protocol: TCP
       - Host Port: 2222 (or any other port you like)
       - Gust port: 22

       ![](https://averagelinuxuser.com/assets/images/posts/2022-05-21-ssh-into-virtualbox/Virtualbox-port-forwarding.jpg)

    3. Reboot host machine and ssh by `ssh -p 2222 virtualbox-user-name@localhost`
 
  </details>

<details><summary>Useful Shell Commands & Links</summary>

### Data Cleansing

- Filtering out lines **shorter** than 30 characters
  
  ```bash
  grep -E '^.{30,}$' input.txt > output.txt
  ```
  
- Removing blank lines

  ```bash
  grep -v '^$' input.txt > output.txt
  ```
  
- Removing Duplicate Lines

  ```bash
  sort {file-name} | uniq
  ```
  
- Sorting Strings and Ordering by Duplicate Counts

  ```bash
  cat data.txt | sort | uniq -c | sort -n
  ```

- Listing Files Sorted by the Number of Lines

  ```bash
  find /group/book/four/word/ -type f -exec wc -l {} + | sort -rn
  ```

- Replacing character with another

  ```bash
  cat data-file | tr char-to-be-replaced new-char
  ```
  
- Lowercasing a File

  ```bash
  tr A-Z a-z < input
  ```

- [Filtering Rows Based on Number of Columns](http://www.theunixschool.com/2012/06/awk-10-examples-to-group-data-in-csv-or.html)

  ```bash
  $ echo '0333 foo
  >  bar
  > 23243 qux' | awk 'NF==2{print}{}'
  0333 foo
  23243 qux
  ```
                    
- Reversing the Order of a List of Words

  ```bash
  echo $str | awk '{ for (i=NF; i>1; i--) printf("%s ",$i); print $1; }'
  ```
                    
- Add Numbers in a File, each Line Containing a Number

  ```bash
  cat file | awk '{ SUM += $1} END { print SUM }'
  ```
                    
- Extracting Substring Within Double Quotes

  ```bash
  $ echo "substring" | cut -d '"' -f2
  substring
  ```
                    
- Removing Anything After a Character(Inclusive)

  ```bash
  $ echo "substring + ?" | cut -f1 -d"+"
  substring
  ```
                    
- GroupBy a CSV File

  ```bash
  cut -d ',' -f 6,7 data.csv | tail -n +2 | awk -F, '{a[$1]+=$2;}END{for(i in a)print i", "a[i];}'
  ```

  - ``cut -d ',' -f first_column_idx,last_column_idx data.csv``: extract a subset of columns and rows from a CSV file
  - ``tail -n +2``: remove the header line(first line) in CSV file
  - ``awk -F, '{a[$1]+=$2;}END{for(i in a)print i", "a[i];}'``: find the sum of individual group records

  For example, suppose we have a data file of:

  ```csv
  Date,Fruit Purchased,Num Purchased
  2020-05-20,apple,10
  2020-05-21,orange,10
  2020-05-22,banana,5
  2020-05-23,apple,10
  2020-05-24,orange,5
  2020-05-25,banana,10
  ```

  Running ``cut -d ',' -f 2,3 data.csv | tail -n +2 | awk -F, '{a[$1]+=$2;}END{for(i in a)print i", "a[i];}'`` gives:

  ```
  apple, 20
  banana, 15
  orange, 15
  ```

### Data Sourcing
  
- [Converting PDF to text](https://www.pdf2go.com/pdf-to-text) 
- Converting PDF to Images

  ```bash
  pdftoppm -rx 300 -ry 300 -png file.pdf prefix # 300 specifies resolution
  ```
  
- Convert .flv to .mp4: [Handbrake](https://handbrake.fr) converts FLV into anything. The process is fairly straightforward:

  1. Start Handbrake.
  2. Click the **Source** button at the top.
  3. Locate and choose the FLV file.
  4. Choose an appropriate preset or configure the **Video** and **Audio** tabs manually.
  5. Click the **Start** button.

</details>
  
### Blacklist
  
- ~~[TypeScript UML Playground](https://github.com/stealth-tech-startup/typescript-uml)~~ We observes that UML related techonologies today are not well maintained in general. The relfects the fact that UML will soon be replaced by a new code analysis paradim 
- ~~[Graphviz](https://softwarerecs.stackexchange.com/q/40)~~: AT&T isn't supporting Graphviz as much as it did in the past and some of the authors have left to seek other work

Tenured Innovations @paion-data
-------------------------------

### Yahoo [Yavin](https://github.com/stealth-tech-startup/framework)

We use Yavin internally to empower our data-based decision making, such as quantifying employees salary bonus & promotion, and analyzing the user behavirous of our product

- [Documentation](https://stealth-tech-startup.github.io/yavin-docs/)
- [Example Yavin App (Template)](https://github.com/stealth-tech-startup/yavin-app)

  - [Externalized Config for the Example App (Template)](https://github.com/stealth-tech-startup/yavin-demo-config)

- [Elide](https://stealth-tech-startup.github.io/elide-doc/)

### Immutable Infrastructure via HashiCorp
------------------------------------------

What [HashiCorp AWS][HashiCorp AWS]  Believes
---------------------------------------------

[HashiCorp AWS][HashiCorp AWS] believes infrastructure is the "home" to software. The _highest-quality_ software are not possible unless backed by
the best-made tech infrastructure

### Traditional Software Development

![Error loading traditional.png](https://github.com/QubitPi/QubitPi/blob/master/img/hashicorp-aws/traditional.png?raw=true)

I learned, from years of work experience, that thriving as a Software Engineer with their internal and external
engagement demands requires high levels of _interpersonal sophistication_. It is no doubt then that the **single
hardest task in teamwork is _efficient communication_**. This gets exacerbated in a software development cycle in which
a developer has to distribute their communication efforts among **3** parties, which makes mis-communication frequent

### How Big Techs Improve It

![Error loading yahoo.png](https://github.com/QubitPi/QubitPi/blob/master/img/hashicorp-aws/yahoo.png?raw=true)

By the time I joined Yahoo at 2016, the company had already made a
[big move by removing all of its QA teams COMPLETELY][Yahoo removed QA]. Software developers were required to write
automated tests by themselves using open source test frameworks, such as Groovy Spock, Jest, and Cypress. The software
testing was then fully automated through [Yahoo's own CI platform][Screwdriver], which is developed on top of
[Jenkins][Jenkins] originally.<br/><br/>This brought a big software quality improvements but in terms of communication
quality, at least from my experience, was still not optimal. I've had such experience when I finshed implementing a
system but waited for extra couple of weeks before DevOps Engineer set up a dedicated server for deployment. This
virtually got mis-translated to my boss as "A software developer had his work delayed for couple weeks".

### Software Development Tomorrow (What _HashiCorp AWS_ Does)

![Error loading new.png](https://github.com/QubitPi/QubitPi/blob/master/img/hashicorp-aws/new.png?raw=true)

The reason we still have DevOps staff is resource isolation using the ubiquitous Docker, which borns out of the
traditional on-premise technology, is _manual_. With on-demand cloud, resource isolations are assumed NOT managed. We
instead _manage business logics_ with efficiency ([Packer][Packer]) and immutability ([Terraform][Terraform]). **With
HashiCorp + OpenStack Cloud, business no longer needs ~~Docker + k8s~~**. Teams and developers as well, with almost no
overhead, are able to eliminate human DevOps<br/><br/>This is the picture from which I'm turning into reality in my
team. Giving our developer fully **automated** control over infrastructure brings the following benefits to the team:

- **Our developers learn more cutting-edge industry skills compared to their peers which makes our developers more
  valuable along their career path**
- **Taking hardware constraint into account causes a paradigm shift in how our engineers thought about problems, which
  makes our developers better skilled and our software better in terms of quality**
- **Eventually reduces the labor costs of company**

[HashiCorp AWS][HashiCorp AWS] does exactly that.

[HashiCorp AWS]: https://github.com/marketplace/actions/hashicorp-aws
