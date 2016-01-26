# Application ideas



#### English master
1. Requirements

2. Technology
    - spring boot
    - angularjs
    - postgresql or mysql

#### Todo Manager

1. Requirements for todo manager
    - cyclic events
    - today checklist

2. Technology
      - nodejs
      - angularjs
      - mongodb
  
#### Stock Advisor
1. Requirements
    - retrive stock data form internet
    - show graphs for choosen company

2. Technology
    - play framework

#### Data generator
1. Requirements
    - pesel generator
    - nip generator
    - regon generator
    - create csv with first name, last name, pesel

2. Technology
    - AngularJS

#### My calendar

1. Requirements
    - add 
    - export to excel

2. Technology
    - AngularJS

##### Usefull links:
[Angularjs and Play Framework](http://www.toptal.com/java/building-modern-web-applications-with-angularjs-and-play-framework)

[Scalajs and Angularjs](http://www.smartjava.org/content/creating-angularjs-application-without-javascript-scalajs)

[Agile - HOW TO SPLIT A USER STORY](http://www.agileforall.com/wp-content/uploads/2012/01/Story-Splitting-Flowchart.pdf)

#####Spring oauth2 logout

``` java
@Controller
public class OAuthController {
    @Autowired
    private TokenStore tokenStore;

    @RequestMapping(value = "/oauth/revoke-token", method = RequestMethod.GET)
    @ResponseStatus(HttpStatus.OK)
    public void logout(HttpServletRequest request) {
        String authHeader = request.getHeader("Authorization");
        if (authHeader != null) {
            String tokenValue = authHeader.replace("Bearer", "").trim();
            OAuth2AccessToken accessToken = tokenStore.readAccessToken(tokenValue);
            tokenStore.removeAccessToken(accessToken);
        }
    }
}
```

#### Looking for car
http://www.opel-insignia.com.pl/viewtopic.php?f=5&t=16200

##### Otomoto

http://allegro.pl/show_item.php?item=5921434845#2202752439

http://otomoto.pl/oferta/seat-leon-seat-leon-st-fr-1-4-tsi-150-km-auto-demonstracyjne-salon-seat-ID6ydztB.html#f8b17c4af8

http://otomoto.pl/oferta/citroen-c4-grand-picasso-2-0-hdi-150-km-more-life-ID6yc0gH.html#094bab2461

http://otomoto.pl/oferta/seat-leon-fr-2-0-tdi-gwarancja-4-lata-dealer-plichta-vw-fv23-ID6ye1nT.html#4f55fd70e6

http://otomoto.pl/oferta/skoda-octavia-rs-2-0-tsi-162-kw-220-km-start-stop-wyprzedaz-2015-ID6y6aEb.html#4f55fd70e6

http://otomoto.pl/oferta/opel-insignia-gwarancja-salon-pl-fv-vat-23-edition-ID6ygpDL.html#8360e04a36


#### Other
http://jakoszczedzacpieniadze.pl/jak-oszczedzac-na-samozatrudnieniu


### Tests
- helpers
    - JaxRsHelper
- invokers
    - UserServicesInvoker
    - QrServicesInvoker
- processes
    - startPageLoading
    - usersRegistration
    - usersAuthentication
    - qrsSaving

#### Java security
https://docs.oracle.com/javase/tutorial/security/apisign/vstep1.html

http://stackoverflow.com/questions/5127379/how-to-generate-a-rsa-keypair-with-a-privatekey-encrypted-with-password
