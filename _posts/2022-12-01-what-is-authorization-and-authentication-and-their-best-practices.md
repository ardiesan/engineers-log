---
layout: post
title: "What is Authorization & Authentication, and their Best Practices"
author: nsagnoy
categories:
- internship
- authentication
- authorization
image: assets/images/authorization_and_authentication.png
---

The availability of today's applications via several networks and connection to the cloud increase their vulnerability to security threats and breaches, making security a crucial issue. There is increasing pressure to ensure application-level security. 
In this article, we will tackle two of the commonly used and effective application security methods, **Authentication and Authorization**.

To deal with sensitive data assets, **Authentication and Authorization** are both necessary. Without any of them, you leave your data open to unwanted access and data breaches. 
While often used interchangeably, authentication and authorization are distinct security processes.

<br>

## What is Authentication?
Authentication is the act of verifying/validating a user's identity by proving that they are who you say you are, commonly through providing valid login credentials. 

A real-world example of this is when an employee enters their office building. Before given access to enter, the security guard will ask for the employee's identification card to verify if the person is indeed an employee of the company. When verified, the employee can now enter the premises. This process also happens when a user tries to use an application.

#### Authentication Methods:
- **Username & Password** - probably the most common authentication method widely used in application development. If the user enters a valid login credentials (username and password), the system assumes the identity is valid and grants access.

<img src="{{ site.baseurl }}/assets/images/login.jpeg" alt="username and password auth" width="800px">

- **One-time Pin/Password** - is a string of characters or numbers that authenticates a user for a single login attempt or transaction. 

<img src="{{ site.baseurl }}/assets/images/otp.jpeg" alt="OTP auth" width="800px">

- **Biometrics** - is a security process that compares a person’s characteristics to a stored set of biometric data in order to grant access to buildings, applications, and systems.

<img src="{{ site.baseurl }}/assets/images/biometric.png" alt="biometrics auth" width="800px">

<br>

## What is Authorization?

Authorization is the process of giving someone the ability to access a resource or service. It determines the level and type of access to resources a user has and answers the questions of who can do what with your data and applications. Once a user successfully log in to an application, their authorization will determine the menu, services and parts of the system user is allowed to see and access. Collectively, these permissions are known as client privileges.

A real-world scenario of this is house ownership. The owner has full access rights to the house and can grant other people permission to access it. You say that the owner authorizes people to enter the house. The owner can roam the whole property and do anything (like renovations, replace furniture, etc.). But guests cannot do these things since they do not have the authority to do so. 

#### Authorization Strategies
- **Attribute-Based Access Control (ABAC)** - is an authorization model that evaluates attributes (or characteristics), rather than roles, to determine access. An example of this authorization process is an online store that sells alcoholic beverages. The online retailer requires buyers to sign up and present identification that verifies their age. The buyer's age is a claim that is verified throughout the registration process and serves as proof of the buyer’s age attribute. Presenting the age claim allows the store to process access requests to buy alcohol. So, in this case, the decision to grant access to the resource is made upon the buyer's attribute.

- **Role-Based Access Control (RBAC)** - assign access and actions according to a person's role within the system. For example, let us say you are a doctor. As a doctor in the hospital, you should have permissions that reflect your role. Thus, you have access to complete patient records, while the receptionist can access only basic contact information.

- **Relationship-Based Access Control (ReBAC)** - is an authorization model where access decisions are based on the relationships a subject has. A well-known examples of relationship-based access control are social networks. In Facebook, for example, you can allow access to your posts and photos to friends of friends.

<br>

## Authentication vs Authorization

<img src="{{ site.baseurl }}/assets/images/Authentication-vs-Authorization.webp" alt="Authentication vs Authorization" width="800px">

<table>
    <thead>
        <tr>
            <th>Authentication</th>
            <th>Authorization</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Usually the first step of a security access control</td>
            <td>Comes after authentication</td>
        </tr>
        <tr>
            <td>Verifies user identity</td>
            <td>Grants or denies permissions to the user to access something</td>
        </tr>
        <tr>
            <td>Common methods: Username &amp; Password, OTP, and Biometrics</td>
            <td>Common methods: Attribute-Based Access Control, Role-Based Access Control, 
and Relationship-Based Access Control</td>
        </tr>
        <tr>
            <td>Visible to the user</td>
            <td>Not visible to the user</td>
        </tr>
        <tr>
            <td>It is changeable by the user</td>
            <td>Cannot be changed by the user</td>
        </tr>
    </tbody>
</table>

<br>

## Authentication and Authorization Best Practices

### Authentication
Here are some of the common best practices for authentication: 

- **Implement HTTPS** - A protocol called Security Sockets Layer (SSL) enables secure and encrypted communication between a client and a server. Without SSL certificates, websites and web apps are equivalent to restaurants without the approval of a food inspector.
  After installing and configuring an SSL certificate, your website or web application may utilize the HTTPS protocol to ensure that any private information of your users—such as login credentials, payment information, and more—transmitted between a browser and a server is encrypted.
  Without HTTPS, user credentials can leak through unprotected networks and hackers can easily eavesdrop and look at the data during data transmission.

- **Salt and Hash Passwords** - To add more security to your password, you must salt the password by adding a string before hashing it. Salting is crucial since it makes it harder for hackers to expose the hash. 
  After salting, the passwords are hashed by passing a one-way function through a mathematical procedure that transforms the password into a different representation.

- **Consider enabling Multi-Factor Authentication** - The good old username and password is not as secure as you think. Sensitive user information can no longer be safeguarded by that thin single layer of defense. MFA is currently often used in web apps to offer extra security levels. Most of the time, a minimum of two factors are needed to authenticate a user, also known as two-factor authentication.

- **Mark Cookies as Secure** - this makes cookie theft harder.

- **Delete all cookies and invalidating sessions** - When a user logs out, ensure to delete all cookies and invalidate sessions. This makes the use of shared computers safer.

- **Session expiry** - Do not create forever-lasting sessions.

- **Use Generic Error Messages** - Don't leak information through error messages. Attackers shouldn't be able to determine if an email is registered or not. If an email is not found, upon login, just report "The user ID or password was incorrect"  or "Incorrect credentials".

### Authorization
Here are some of the common best practices for authorization:

- **Design and Implement Authorization early in the Software Development Lifecycle** - Early in the software development process, authorization functionality should be planned. It makes us consider the fundamental prerequisites for roles and privileges, which will be much more useful as the application's complexity increases.

- **Utilize Authorization Middleware** - Short-lived permission permits are preferred, and the server should continuously authorize each request. This may be done by using authorization middleware and making sure that only the authorization middleware handles requests to and from the server. This avoids the risk of unprotected API endpoints and URL paths.

- **Implement Authorization Policies** - Authorization policies allow administrators to implement fine-grained access controls. The capacity to allow or prohibit access to critical resources, such as data and resources, depending on multiple requirements and/or entitlements to a single data resource is known as fine-grained access control.

- **Maintain Authorization State on the server-side** - Similar to an authentication state, an authorization state must always be kept on the server-side. HTTP request headers, source addresses, unsigned cookies, and access tokens can be easily tampered with and modified. Always sign and validate session data to reduce the chance of session tampering. Cross-site request forgery (CSRF) tokens and session cookies should be used to manage the authorization session, and the server should sign both values.

<br>

## Conclusion
Authentication and authorization are both important information security processes that administrators utilize to secure systems and information. To simply put, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.
They determine a system's security when combined. Thus, one cannot have a secure system unless you have configured both authentication and authorization correctly.