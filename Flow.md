## How to use the service ? 

- Register your service to use with the Who service. 
  - Reach out to support[at]afila.fyi for onboarding.
  - Upon registration, you will be provided with JWT token keys that identify your identity with the service.
    - Please provide the token in the Authorization header for your verification web request. 

- When validating a phone number supplied by the user,
  - Generate a challenge code, and make a call to the Who verification endpoint along with the phone number, challenge code, and a unique session guid.
    - This call will return a Validated (if the phone number was validated) or a Failure message if the request was not validated in time.
  - Make sure that the user/application must be able to see the generated challenge code.

- The Who service will send a verification link using an SMS that's sent to the supplied phone number. 
- User is able to enter the challenge code by clicking on the link in the SMS message.
- Once a successful challenge code is supplied, the Who service will return a "Validated" response to the service.
