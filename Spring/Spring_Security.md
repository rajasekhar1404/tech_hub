### 1.What is Spring Security?
- Spring Security is a framework which provides authentication and authorization capabilities to the java application
#### the key features of spring  security are :
- Authentication : provides user authentication through various mechanisms like username/password,token,ldap
- Authorization : controlling the access to the user based on their roles and permissions
- Session Management : Managing user sessions, including session fixation protection, concurrent session control, etc.
- CSRF Protection : prevents from cross site request forgery attacks
- Remember Me Functionality:Allowing users to be remembered between sessions.
- Integrations with other frameworks and technologies like spring mvc, OAuth, etc
### 2. Explain the authentication flow in Spring Security.
- When ever user tries to access the secured resources the following steps occurs
- user submits the login credentials 
- credentials are validated by  authentication provider (eg. database or ldap)
- if it is valid it creates a authentication object
- authentication object is stored in security context
- the user is considered authenticated and granted access to the requested resources
### 3.How can you configure method-level security in Spring Security?
- Method level security is provided by using @PreAuthorize and @PostAuthorize
- @PreAuthorize 
- @PostAuthorize 
### 4. What is CSRF protection, and how can you enable it in Spring Security?
- CSRF (cross site request forgery) protection prevents from malicious websites give unauthorized request on behalf of the user
- spring security provides  generating and validating  unique tokens associated with user sessions
- to enable spring security we can use csrf() method in security configuration
