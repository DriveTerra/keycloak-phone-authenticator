# keycloak-phone-authenticator

## What This Is
Custom Keycloak SPI (Service Provider Interface) extension that adds phone/SMS-based authentication to Keycloak. Enables OTP login via SMS and WhatsApp.

## Stack
- **Language**: Java
- **Framework**: Keycloak SPI
- **SMS Provider**: AWS SNS
- **WhatsApp Provider**: Twilio

## Features
- Phone number registration and verification
- SMS OTP generation and validation
- WhatsApp OTP via Twilio
- Custom authentication flow integration with Keycloak
- Provider factories for pluggable SMS/WhatsApp backends

## Key Files
- `src/main/java/` — SPI implementations
- Provider factories for SMS (AWS SNS) and WhatsApp (Twilio)
- Custom authenticator flow definitions

## Conventions
- Keycloak SPI pattern — implement provider interfaces, register via provider factories
- Deployed as a JAR into Keycloak's providers directory
- Configuration via Keycloak admin console (realm settings)

## Related Services
- Keycloak 22.0.5 (in Backend-Infrastructure)
- Used by: All frontend apps and mobile apps for login
