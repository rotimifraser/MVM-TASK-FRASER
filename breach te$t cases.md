| Test Case ID | Test Case Title | Test Suite / Module Name | Related Requirement(s) | Test Priority | Preconditions | Test Data | Test Steps / Procedure | Expected Result | Actual Result | Pass/Fail Status | Postconditions / Cleanup | Environment | Tested By | Date Executed | Defect/Bug ID | Evidence Link | Remarks / Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| TC001 | Verify user can navigate to Home Page via provided URL | Navigation | NAV-001 | High | User has a browser and internet access | https://breach-fe.qa.mvm-tech.xyz/ | 1. Launch browser
2. Enter the URL
3. Press Enter | User is navigated to the Home Page |  |  |  | QA |  |  |  |  |  |
| TC002 | Verify both 'Join Breach' buttons navigate to registration page | Navigation | NAV-002 | High | User is on Home Page | N/A | 1. Click first 'Join Breach' button
2. Verify navigation
3. Return to Home Page
4. Click second 'Join Breach' button
5. Verify navigation | Both buttons navigate to the Registration Page |  |  | Return to Home Page | QA |  |  |  |  | Verify that buttons are visually distinct |
| TC003 | Verify Continue button is disabled with invalid/empty input | Registration | REG-001 | High | User is on Registration Page | Empty email and password fields | 1. Leave email and password blank
2. Check state of Continue button | Continue button is disabled |  |  |  | QA |  |  |  |  |  |
| TC004 | Verify Continue button is enabled with valid input | Registration | REG-002 | High | User is on Registration Page | Email: test@example.com
Password: Test@1234 | 1. Enter valid email
2. Enter valid password
3. Check state of Continue button | Continue button is enabled |  |  |  | QA |  |  |  |  |  |
| TC005 | Verify presence of Breach logo at top right | Registration UI | UI-001 | Medium | User is on Registration Page | N/A | 1. Observe top right section of the page | Breach logo is present |  |  |  | QA |  |  |  |  |  |
| TC006 | Verify back button navigates to Home Page | Navigation | NAV-003 | Medium | User is on Registration Page | N/A | 1. Click the back button on the top right | User is redirected to the Home Page |  |  |  | QA |  |  |  |  |  |
| TC007 | Verify 'Already have an account' link navigates to Login Page | Navigation | NAV-004 | Medium | User is on Registration Page | N/A | 1. Click on 'Already have an account?' text | User is navigated to the Login Page |  |  |  | QA |  |  |  |  |  |
| TC008 | Verify 'Terms and Conditions' link works | Navigation | NAV-005 | Low | User is on Registration Page | N/A | 1. Click on 'Terms and Conditions' text | User is navigated to the Terms and Conditions page |  |  |  | QA |  |  |  |  |  |
| TC009 | Verify static text at top of Registration Page | Registration UI | UI-002 | Low | User is on Registration Page | N/A | 1. Observe text at top of page | Text should say: 'Join Breach
Break through the noise and discover content that matters to you in under 3 minutes.' |  |  |  | QA |  |  |  |  | Text formatting should be checked |
| TC010 | Verify system handles extremely long email addresses | Validation - Email | VAL-001 | High | User is on Registration Page | Email: aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa@bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb.com | 1. Enter an extremely long valid email address
2. Enter valid password
3. Observe behavior of Continue button | Email is accepted if within system limits; Continue button is enabled |  |  |  | QA |  |  |  |  | RFC allows 320 characters; test UI and backend limit |
| TC011 | Verify invalid email formats are rejected | Validation - Email | VAL-002 | High | User is on Registration Page | Invalid emails: user@, user.com, @domain.com | 1. Enter invalid email format in email field
2. Enter valid password
3. Try to enable Continue button | Continue button remains disabled; error shown if applicable |  |  |  | QA |  |  |  |  | Test multiple invalid formats |
| TC012 | Verify rejection of SQL injection in email field | Validation - Security | SEC-001 | High | User is on Registration Page | Email: test@example.com' OR '1'='1 | 1. Enter email with SQL injection string
2. Enter valid password
3. Check if Continue button is enabled | Input is rejected or ignored; Continue remains disabled |  |  |  | QA |  |  |  |  | Ensure input is sanitized |
| TC013 | Verify system accepts complex and long password | Validation - Password | VAL-003 | Medium | User is on Registration Page | Password: Aa1!Aa1!Aa1!Aa1!Aa1!Aa1!Aa1!Aa1! | 1. Enter valid email
2. Enter complex, long password
3. Check Continue button | Continue button is enabled |  |  |  | QA |  |  |  |  |  |
| TC014 | Verify system rejects script injection in password | Validation - Security | SEC-002 | High | User is on Registration Page | Password: <script>alert('x')</script> | 1. Enter valid email
2. Enter malicious password
3. Check if input is escaped or rejected | Script input is sanitized or rejected; no execution or risk |  |  |  | QA |  |  |  |  | Ensure XSS protection in place |
| TC015 | Verify user can navigate to Home Page via provided URL | Navigation | NAV-006 | High | User has a browser and internet access | https://breach-fe.qa.mvm-tech.xyz/ | 1. Launch browser
2. Enter the URL
3. Press Enter | User is navigated to the Home Page |  |  |  | QA |  |  |  |  |  |
| TC016 | Verify 'Login' button navigates to Login Page | Navigation | NAV-007 | High | User is on Home Page | N/A | 1. Click the 'Login' button
2. Verify navigation to the Login Page | User is navigated to the Login Page |  |  |  | QA |  |  |  |  |  |
| TC017 | Verify 'Continue' button is disabled with empty/invalid input | Login - Validation | LOG-001 | High | User is on Login Page | Empty email and password fields | 1. Leave email and password blank
2. Check if 'Continue' button is disabled | The 'Continue' button remains disabled |  |  |  | QA |  |  |  |  |  |
| TC018 | Verify 'Continue' button is enabled with valid input | Login - Validation | LOG-002 | High | User is on Login Page | Email: test@example.com
Password: Test@1234 | 1. Enter valid email
2. Enter valid password
3. Check if 'Continue' button is enabled | The 'Continue' button is enabled |  |  |  | QA |  |  |  |  |  |
| TC019 | Verify presence of Breach logo at top right of Login Page | UI - Login | UI-003 | Medium | User is on Login Page | N/A | 1. Observe top right section of the Login Page | Breach logo is present at the top right |  |  |  | QA |  |  |  |  |  |
| TC020 | Verify 'Back' button navigates to Home Page | Navigation | NAV-008 | Medium | User is on Login Page | N/A | 1. Click the back button at the top right | User is redirected to the Home Page |  |  |  | QA |  |  |  |  |  |
| TC021 | Verify 'Don't have an account' link navigates to Registration Page | Navigation | NAV-009 | Medium | User is on Login Page | N/A | 1. Click on 'Don't have an account?' text | User is navigated to the Registration Page |  |  |  | QA |  |  |  |  |  |
| TC022 | Verify 'Terms and Conditions' link works on Login Page | Navigation | NAV-010 | Low | User is on Login Page | N/A | 1. Click on 'Terms and Conditions' text | User is navigated to the Terms and Conditions page |  |  |  | QA |  |  |  |  |  |
| TC023 | Verify static text at top of Login Page | UI - Login | UI-004 | Low | User is on Login Page | N/A | 1. Observe text at top of page | Text should say: 'Join Breach
Break through the noise and discover content that matters to you in under 3 minutes.' |  |  |  | QA |  |  |  |  | Check that the formatting is correct |
| TC024 | Verify system handles extremely long email addresses on Login Page | Validation - Email | VAL-004 | High | User is on Login Page | Email: aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa@bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb.com | 1. Enter an extremely long valid email address
2. Enter valid password
3. Check 'Continue' button | Email is accepted if within system limits; Continue button is enabled |  |  |  | QA |  |  |  |  | RFC allows 320 characters; check limits |
| TC025 | Verify invalid email formats on Login Page are rejected | Validation - Email | VAL-005 | High | User is on Login Page | Invalid emails: user@, user.com, @domain.com | 1. Enter invalid email format
2. Enter valid password
3. Check if 'Continue' button remains disabled | Error message shown for invalid email formats |  |  |  | QA |  |  |  |  | Test various invalid formats |
| TC026 | Verify system rejects SQL injection in email field on Login Page | Validation - Security | SEC-003 | High | User is on Login Page | Email: test@example.com' OR '1'='1 | 1. Enter email with SQL injection string
2. Enter valid password
3. Check if 'Continue' button is enabled | Input is rejected or sanitized |  |  |  | QA |  |  |  |  | Ensure input is sanitized |
| TC027 | Verify successful registration returns user ID and token | Registration - API Response Validation | REG-010 | High | User completes registration with valid credentials | Email: user@example.com
Password: ValidPass123! | 1. Complete registration form
2. Click 'Continue'
3. Intercept response payload | Response should contain valid user ID and token |  |  | Store token for authenticated session | QA |  |  |  |  | Validate token format and UUID for ID |
| TC028 | Verify successful login returns user ID and token | Login - API Response Validation | LOG-006 | High | User has an existing account | Email: user@example.com
Password: ValidPass123! | 1. Enter login credentials
2. Click 'Continue'
3. Intercept login response | Response contains valid user ID and token |  |  | Store token for authenticated session | QA |  |  |  |  | Confirm authentication session |
| TC029 | Verify redirection to user dashboard after successful login | Login - Navigation | LOG-007 | High | User is logged in successfully | N/A | 1. Complete login with valid credentials
2. Observe redirection | User is redirected to their home/dashboard page |  |  |  | QA |  |  |  |  | Ensure session is active on dashboard |
| TC030 | Verify invalid login returns appropriate error message | Login - Validation | LOG-008 | High | User attempts login with incorrect credentials | Email: user@example.com
Password: WrongPassword! | 1. Enter incorrect login details
2. Click 'Continue' | User sees error message like 'Invalid credentials' |  |  |  | QA |  |  |  |  | Check error display timing and format |
| TC031 | Verify login fails gracefully with expired token | Login - Security | SEC-004 | Medium | User token has expired | Expired token from previous session | 1. Attempt to access protected route with expired token | User is logged out and redirected to login page |  |  | Clear expired token | QA |  |  |  |  | Security check for session expiration |
| TC032 | Verify 'Start Writing' button opens post creation modal | Main Screen - Functionality | MAIN-001 | High | User is logged in and on main screen | N/A | 1. Click on 'Start Writing' button at top left
2. Observe UI response | Post creation modal should appear |  |  |  | QA |  |  |  |  | Currently this functionality is not working |
| TC033 | Verify 'Home' side button keeps user on home screen | Main Screen - Navigation | MAIN-002 | Medium | User is logged in and on main screen | N/A | 1. Navigate to any other page (if possible)
2. Click on 'Home' side button
3. Observe screen | User should remain on or return to home screen |  |  |  | QA |  |  |  |  | Confirm visual indication of active state |
| TC034 | Verify 'Dashboard' side button navigation | Main Screen - Navigation | MAIN-003 | High | User is logged in and on main screen | N/A | 1. Click on 'Dashboard' side button
2. Monitor network activity
3. Observe screen changes | User should navigate to dashboard; API calls should occur |  |  |  | QA |  |  |  |  | Currently no API calls are made - functionality not working |
| TC035 | Verify 'Publication' side button navigation | Main Screen - Navigation | MAIN-004 | High | User is logged in and on main screen | N/A | 1. Click on 'Publication' side button
2. Monitor network activity
3. Observe screen changes | User should navigate to publication page; API calls should occur |  |  |  | QA |  |  |  |  | Currently no API calls are made - functionality not working |
| TC036 | Verify 'Feature' navbar displays appropriate content | Content Display | CONT-001 | High | User is logged in and on main screen | N/A | 1. Click on 'Feature' navbar
2. Observe content displayed | Content should update to show featured blog posts |  |  |  | QA |  |  |  |  | Currently only showing dummy data |
| TC037 | Verify 'Popular' navbar displays appropriate content | Content Display | CONT-002 | High | User is logged in and on main screen | N/A | 1. Click on 'Popular' navbar
2. Observe content displayed | Content should update to show popular blog posts |  |  |  | QA |  |  |  |  | Currently only showing dummy data |
| TC038 | Verify 'Recent' navbar displays appropriate content | Content Display | CONT-003 | High | User is logged in and on main screen | N/A | 1. Click on 'Recent' navbar
2. Observe content displayed | Content should update to show recent blog posts |  |  |  | QA |  |  |  |  | Currently only showing dummy data |
| TC039 | Verify Stream section displays trending content | Content Display | CONT-004 | Medium | User is logged in and on main screen | N/A | 1. Observe the stream section on the far right
2. Check if content is based on user preferences | Stream should show trending content based on user preferences |  |  |  | QA |  |  |  |  | Currently only showing dummy data |
| TC040 | Verify layout integrity on MacBook 13" | Compatibility - Desktop | COMP-001 | High | Application loaded on MacBook 13" screen | N/A | 1. Log in to application
2. Observe all UI elements on main screen
3. Check navigation options
4. Check content display | All elements should be properly displayed and functional |  |  |  | QA | MacBook 13" |  |  |  | Verify spacing, alignment, and readability |
| TC041 | Verify layout and functionality on iPhone 15 | Compatibility - Mobile | COMP-002 | High | Application loaded on iPhone 15 | N/A | 1. Log in to application
2. Observe UI layout
3. Check for presence of side navbars
4. Attempt to access navbar functionality | Side navbars should adapt to mobile view with accessible functionality |  |  |  | QA | iPhone 15 |  |  |  | Currently side navbars disappear with no alternative access method |
| TC042 | Verify layout and functionality on iPad Mini | Compatibility - Tablet | COMP-003 | High | Application loaded on iPad Mini | N/A | 1. Log in to application
2. Observe UI layout
3. Check for presence of side navbars
4. Attempt to access navbar functionality | Side navbars should adapt to tablet view with accessible functionality |  |  |  | QA | iPad Mini |  |  |  | Currently side navbars disappear with no alternative access method |
| TC043 | Verify application compatibility with Safari browser | Compatibility - Browser | COMP-004 | High | Safari browser is installed | N/A | 1. Open application in Safari
2. Complete login
3. Test all main screen functionality
4. Check rendering of all UI elements | Application should function correctly in Safari browser |  |  |  | QA |  | Safari |  |  | Check for any Safari-specific rendering issues |
| TC044 | Verify application compatibility with Chrome browser | Compatibility - Browser | COMP-005 | High | Chrome browser is installed | N/A | 1. Open application in Chrome
2. Complete login
3. Test all main screen functionality
4. Check rendering of all UI elements | Application should function correctly in Chrome browser |  |  |  | QA |  | Chrome |  |  | Check for any Chrome-specific rendering issues |
| TC045 | Verify application compatibility with Firefox browser | Compatibility - Browser | COMP-006 | High | Firefox browser is installed | N/A | 1. Open application in Firefox
2. Complete login
3. Test all main screen functionality
4. Check rendering of all UI elements | Application should function correctly in Firefox browser |  |  |  | QA |  | Firefox |  |  | Check for any Firefox-specific rendering issues |
| TC046 | Verify responsive behavior when resizing browser window | Compatibility - Responsiveness | COMP-007 | Medium | Application loaded on desktop browser | N/A | 1. Load application at full browser size
2. Gradually decrease browser width
3. Observe UI adaptation at different breakpoints | UI should adapt gracefully at common breakpoints |  |  |  | QA |  |  |  |  | Check for layout issues during transition |
| TC047 | Verify post creation modal functionality | Main Screen - Functionality | MAIN-005 | High | User has clicked 'Start Writing' button | N/A | 1. Enter post title
2. Enter post content
3. Click submit/publish button
4. Monitor network activity | Post should be created and saved; API calls should occur |  |  |  | QA |  |  |  |  | Currently modal functionality not working |
| TC048 | Verify navigation with keyboard shortcuts | Accessibility | ACC-001 | Low | User is logged in and on main screen | N/A | 1. Test common keyboard shortcuts (Tab, Space, Enter)
2. Check if focus indicators are visible
3. Try to navigate using only keyboard | Essential functionality should be accessible via keyboard |  |  |  | QA |  |  |  |  | Important for accessibility compliance |
| TC049 | Verify screen reader compatibility | Accessibility | ACC-002 | Low | Screen reader software is active | N/A | 1. Navigate through application using screen reader
2. Check if all elements are properly announced
3. Test interactive elements | All elements should be properly labeled for screen readers |  |  |  | QA |  |  |  |  | Important for accessibility compliance |
| TC050 | Verify side navbar behavior on window resize | Responsiveness | RESP-001 | Medium | Application loaded on desktop browser at full width | N/A | 1. Slowly resize browser window smaller
2. Note at which breakpoint navbars change behavior
3. Continue to smallest width | Side navbars should adapt or transform at appropriate breakpoints |  |  |  | QA |  |  |  |  | Identify exact breakpoint where navbars disappear |
| TC051 | Verify alternative navigation on mobile when sidebars disappear | Responsiveness | RESP-002 | High | Application loaded on mobile device | N/A | 1. Log in on mobile device
2. Look for hamburger menu or alternative navigation
3. Test if all navigation options are accessible | There should be alternative access to navigation options |  |  |  | QA |  |  |  |  | Currently no alternative is provided - bug |
| TC052 | Verify content scrolling behavior on mobile devices | Responsiveness | RESP-003 | Medium | Application loaded on mobile device with limited screen space | N/A | 1. Log in on mobile device
2. Scroll through content area
3. Check for smooth scrolling and proper content display | Content should scroll smoothly without layout issues |  |  |  | QA |  |  |  |  | Check for content clipping or overflow |
| TC053 | Verify error handling when API calls fail | Error Handling | ERR-001 | High | User is performing actions that trigger API calls | Network connection interrupted or backend errors | 1. Perform action that requires API call
2. Simulate network failure or error response
3. Observe application behavior | Application should display appropriate error message and handle gracefully |  |  |  | QA |  |  |  |  | Check for user-friendly error messages |
| TC054 | Verify content loading states and indicators | UI - Feedback | UI-005 | Medium | User navigates between content sections | N/A | 1. Click between Feature/Popular/Recent navbars
2. Observe UI during content loading | Loading indicators should display during content retrieval |  |  |  | QA |  |  |  |  | Check for proper loading states to prevent UI jumping |
| TC055 | Verify application behavior with extremely slow network | Performance | PERF-001 | Medium | Application under slow network conditions | Network throttling enabled | 1. Enable network throttling (e.g., 3G slow)
2. Log in and navigate through application
3. Observe application behavior | Application should handle slow connections gracefully |  |  |  | QA |  |  |  |  | Check for timeout handling and user feedback |
| TC056 | Verify Stream section personalization with different user profiles | Personalization | PERS-001 | Medium | Multiple test accounts with different preferences | Different user accounts | 1. Log in with first test account
2. Note content in Stream section
3. Log out and log in with different account
4. Compare Stream content | Stream content should differ based on user preferences |  |  |  | QA |  |  |  |  | Currently shows only dummy data; future test |
