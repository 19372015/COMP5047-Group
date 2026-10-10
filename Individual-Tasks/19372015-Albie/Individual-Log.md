This is a log of my individual document.

19372015
<br> <br>
06/10/2026 [TASK 2]

- Created individual document
- Created contents page
- Begun task 2
- Decided on Functional Requirement: FR-ST-2.1
- Revisit Week 2 lecture slides to familiarise myself with desired format 
- **Wrote +3 quality requirements (Security and Privacy protection)**
  - Student access authentication: "When a student initiates an attempt to unlock an electronic lock with their mobile app, the system should ensure that the student is authenticated as a student on the system and has the student permission level before unlocking the door. All unauthorised access attempts should fail."
  - Secure network communication: "When the mobile application communicates with the access control service over the network, it should use industry standard encryption in its communication, such as TLS 1.3. No information should be sent in plaintext."
  - Secure NFC/BLE communication: "When the mobile application communicates with the electronic lock (NFC/BLE), wireless communications should be encrypted using industry standard encryption such as AES-128/AES-256 to prevent interception."
<br>
09/10/2026 [TASK 2]

- Small grammar fixes
- **Wrote introduction for quality attribute: Security and Privacy protection** 
  - Security and Privacy protection is very important regarding FR-ST-2.1. Unlike a traditional key and lock system, going digital and electronic solves issues, but also introduces new ones. This involves the student's sole way of accessing buildings, so it must be robust. Poor security and privacy protection may lead to unauthorised access to buildings, incepted or manipulated data, and more.
- **Wrote +2 quality requirements (Security and Privacy protection)**
  - Strict credential availability: "The system should identify expired, revoked or invalid digital access credentials, and reject all access attempts regarding that credential."
  - Set lock list: "When a student initiates an attempt to unlock an electronic lock outside of their permitted doors list (students should have an assigned list of doors they are allowed to enter, not all student doors), the system should deny access."
- **Wrote introduction for quality attribute: Performance**
  - "Performance must be sharp and responsive. The system should quickly process and authenticate unlock attempts. Fast response times are important to ensure students can avoid delays caused by the system. As something that replaces physical locks, they are supposed to be the same level of, if not with higher, convenience. Students should not have to wait around during slow communication or system errors."
- **Wrote +3 quality requirements (Performance):**
  - Response time: During normal conditions, when an authenticated student initiates an attempt to unlock a valid door, the system should receive the request, check for valid credentials, and grant either access or denied access, all within five seconds.
  - Heavy traffic performance: During heavy traffic access periods, the digital key access service should continue to function as usual (5 second or less response time) during at least fifty simultaneous requests.
  - Mobile application performance: When a student uses the mobile application and navigates to the page where they can initiate an unlock attempt, load times should take no longer than five seconds.
<br>
10/10/2026 [TASK 2]

- Went through current task 2 and renamed relevant instances of "should" to "shall" because it sounds more strict
- **Wrote introduction for quality attribute: Reliability:**
  - "Reliability concerns the system's ability to be consistent in its operation. Inconsistencies can be dangerous, when physical buildings and places of residence are on the line.The system must successfully grant access when the request is authorised and deny access when authorisation fails"
- **Wrote +6 quality requirements (Reliability)**
  - General availability: The system shall achieve at least 99.9% uptime throughout the operating year, excluding any organised maintenance.
  - Valid request reliability: During normal conditions, when a valid, authorised request is made, the electronic lock shall commence its unlock sequence 99.9% of the time.
  - Invalid request reliability: During normal conditions, when an invalid, unauthorised request is made, the electronic lock shall deny access 100% of the time.
  - Handling failed communication: When communication between the mobile application and the access control system is interrupted, this interruption shall be detected and display a relevant message on the mobile application.
  - Handling duplicate requests: When the same unlock request is sent simultaneously or too swiftly due to a timeout or other error, the system shall handle the request as one, instead of attempting to process the same request multiple times in succession.
  - Recovery time: When a failure occurs, the system shall recover and restore normal operation within twenty minutes.
  - Overall failure rate: The system shall operate as usual with a failure rate lower than three critical failures per operating year.
