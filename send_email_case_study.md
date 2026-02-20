# Case Study: The send_email.py Authentication Saga

This document provides a detailed, chronological breakdown of the cascading platform failures that completely blocked the development of a simple command-line email utility, .

## Attempt 1: Standard OAuth 2.0 (via GUI)

The initial and most straightforward approach to authentication was to use the standard OAuth 2.0 flow for desktop applications. This method failed due to a combination of platform misconfiguration and severe GUI bugs.

### 1.1 Platform Misconfiguration

The default OAuth 'Desktop app' credentials created through the Google Cloud Console were non-functional out of the box. They were missing the required  redirect URI, a critical component for the OAuth flow to complete successfully.

### 1.2 Impassable GUI

Attempts to manually correct the missing redirect URI in the Google Cloud Console were thwarted by a series of critical UI bugs, rendering the interface unusable. These included:

*   **'Unscrollable UI' bug:** This bug prevented scrolling within the UI, effectively hiding the input fields necessary to add or edit the redirect URI.
*   **'Menu Focus Trap':** This bug caused keyboard focus to become trapped within a UI element, making it impossible to navigate to other parts of the page or save any changes.
