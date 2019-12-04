# OAUTH-Authentication

An OATH token is a secure one time password that can be used for two factor authentication.  The first factor is something you know (a password, mother's maiden name) while the second factor is something you have (a smartphone, email address, etc.).  The OATH token is sent to something you have as a one time password to increase security in authentication.

## Uses for OAUTH

**Self service password reset** - When users are locked out or forget their passwords, you need an additional means of verifying their identity.  The traditional method is a series of knowledge based questions (mother's maiden name, eye color, etc).  However, since most of this information can be gleaned from social media profiles, an OATH token as a second factor is almost mandatory to determine the user's identity.

**Step up authentication** - Once your users are already authenticated, you may want to increase the level of security based on what they are accessing.  An example of this is when your user is attempting to access the financial reports for the 10K report.  They have already entered their username and password, but you want to have that second factor for both security and auditing reasons when they access a resource with a higher security level.

**Single sign on to cloud applications** - This use case is similar to the previous step up authentication, but is more broadly applied.  If you are offering single sign on (SSO) to internal applications, you might want to step up the authentication before leaving the network to access cloud applications.  This extra level of authentication coupled with Federation or Web Access Management keeps your SaaS applications doubly secure and your CISO happy with precautions you are taking with the cloud.

**Admin or executive accounts** -I have always found it interesting that the users with the highest privileges tend to get away with the lowest security  --  admins because they control security and CxOs because they sign the admins' checks.  These are exactly the users who should have multi factor authentication and OATH tokens are a fairly innocuous way to deliver that security.  Plus, it gives them a chance to look at their phones in meetings!

**After x number of incorrect authentication attempts** - This use case requires a fairly powerful workflow based IAM platform like EmpowerID that can re-route the authentication requirements based on calculations or an algorithm.  This can be applied to any of the use cases above but is especially useful to prevent hacking attempts.
