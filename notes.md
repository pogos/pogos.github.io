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



##### Usefull links:
[Angularjs and Play Framework](http://www.toptal.com/java/building-modern-web-applications-with-angularjs-and-play-framework)

[Scalajs and Angularjs](http://www.smartjava.org/content/creating-angularjs-application-without-javascript-scalajs)

[Agile - HOW TO SPLIT A USER STORY](http://www.agileforall.com/wp-content/uploads/2012/01/Story-Splitting-Flowchart.pdf)

#####Spring oauth2 logout

```
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
