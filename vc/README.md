# Verifiable Credentials Issuer and Verifier 

## How to issue your own credentials from Azure AD B2C

You need to follow setup procedure for enabling Verifiable Credentials in your Azure AD Premium tenant. The docs can be found [here](https://didproject.azurewebsites.net/docs/issuer-setup.html).

Note that you will not use this Azure AD tenant as the Identity Provider for the issuing of the VC. You just need to configure it in AAD due to license reasons. 

When you come to the part where you edit the Display and the Rules file, you must have your Azure AD B2C tenant ready, because Rules file contains a reference to the well-known openid-configuration. You can either setup a simple User Flow that can be used during issuance of the VC, or you use the [SignUpOrSignin.xml](/b2c/SignUpOrSignin.xml) custom policy in this repo.

For the Display and the Rules file, there are alot of `Yourtenant` everywhere which you can translate into what you want to call your VC card.

## Issuer

The issuer folder contains the node.js sample issuer app and once you have completed the above configuration, you can continue to deploy the sample issuer.

## Verifier 

The verifier folder contains the node.js sample verifier and you can start deploying it after you are done with the issuer. You will be able to test scanning the QR code without uploading the B2C Custom Policies.