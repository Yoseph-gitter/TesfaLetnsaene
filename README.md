# TesfaLetnsaene

This software is designed to create a virtual classroom environment for less fortunate students and teachers. It allows the teacher to create content for students in a certain grade and also provides functionality to create homeworks, assignments, quizs and greade reports.

Up on completion it allows the student to take a pre-recoded lessen in different formats be it in video or text as well as graphical and pictorially.

Requirement: 

1. Teacher should be able to create course outline for a course
2. Teacher should be able to create course content
3. Teacher should be able to create , update course results or grades of students
4. Teacher should have an admin previllage to do all this
5. Students should be able to login to the app using a proper credientials
6. Students should be assigned to a given class before they are allowed to access or take a given course(They can take the course but with out being assigned in a class no course result will be tracked by the system)
7. Application should be able to provide a students report(certeficate) could be for a single class or for a range of years
8. Student should be able to write a complient, comment or suggestion o about his report, exams etc.
9. Application user should be able to send his course result to an email or emails.
10. Course should be designed in to chapters and each chapter in to sections or pages that will be displayed at once on a page
11. Application should allow pagination
12. Application should track student's progress of complition
13. Application should show sections which are complited from those not-complited
14. Application will be designed in a client-server architecture
15. Application's User Interface can be a web or a stand alone Java app
16. Sometime in the future application should support matematical visualizations or graphs for maths and physics courses
17. 

2026 Resume 

Software Engineer / SDET
FINRA — Testing & Continuing Education (TCE) Platform
2024 – 2026 | Rockville, MD (Hybrid)

Served as a dual-role Software Engineer and SDET on the TCE platform — a suite of Java-based microservices and Angular frontends supporting FINRA's candidate registration, exam scheduling, item banking, and regulatory reporting systems. Contributed across the full delivery lifecycle: backend development, platform modernization, REST API design, test automation architecture, and security analysis.

Platform Modernization — Java 17 Upgrade (CRCP, FWS, COPS-Jobs-App, CRD-Snapshot)

Upgraded COPS-Jobs-App from Java 8 / Spring Boot 2.7 / Hibernate 5 → Java 17 / Spring Boot 3.4 / Hibernate 6, touching 35 source files and 1,768+ unit tests

Migrated 163+ files from javax.* → jakarta.* while correctly preserving JDK-owned javax.sql.* / javax.xml.* — a distinction that caused production ClassNotFoundException on Tomcat 10 when misapplied

Removed HibernateTemplate / HibernateDaoSupport across 25+ DAO classes; diagnosed and resolved No CurrentSessionContext configured and TransactionRequiredException with documented short-term bridge and phased long-term refactoring plan

Migrated AWS SES SDK v1 → v2 ahead of December 2025 EOL; reduced FWS WAR size from 157 MB → 107 MB by eliminating duplicate transitive dependencies

Fixed ECS deployment instability: scoped replacetoken, guarded startup scripts with set +e, resolved 4× duplicate scheduler thread pool bug by splitting root/servlet Spring contexts

Produced phased upgrade plans for COPS-Common covering 4 phases with effort estimates, risk ratings, and rollback procedures

Test Automation — ItemBanking Platform (Playwright / TypeScript)

Architected a POM-based Playwright TypeScript framework with environment-aware config, FINRA SSO multi-step auth fixtures, and separate API/UI test layers

Authored end-to-end ItemBank CRUD tests (login → item edit → rationale → save → copy) validated against QA

Led framework selection analysis (Playwright TS vs Playwright Java vs Selenium 4 Java) producing a weighted decision matrix adopted by the team

REST API Design — Scheduling Platform (QEP-Domain)

Designed a 20+ endpoint OpenAPI 3.0 Swagger spec replacing three legacy SOAP services (PVS1/PVS2/PVS3), covering enrollments, appointments, programs, vendors, centers, calendar, and metadata

Defined idempotency semantics, fee determination extraction, full appointment state machine, OAuth 2.0 scope matrix, and PVS parity mapping — with sequence diagrams for all key flows

Security Analysis — FIDO2/WebAuthn Onboarding

Analyzed WebAuthn registration/authentication ceremonies; produced OpenAPI spec for 4 FIDO2 endpoints with full credential option schemas; documented rpId, attestation, session binding, and fallback strategy

Security Engineering — Blind XSS Remediation (CSP)

Audited 6 proxied applications for external resource dependencies; designed a union CSP for shared Apache mod_headers.conf blocking exfiltration while preserving app-level CSP restrictions; documented over-permissive risks with per-domain justifications

Key Technologies: Java 17 · Spring Boot 3 · Hibernate 6 · JUnit 5 · Playwright · TypeScript · OpenAPI 3.0 · AWS SDK v2 · ECS · Docker · Tomcat 10 · PostgreSQL · Maven · Gradle · Jenkins · FIDO2/WebAuthn · Apache HTTPD · CSP · OAuth 2.0 / JWT

Second Version

# Yoseph Hailu

Software Engineer · SDET

> Note: each bullet below has extra context (the *why*, the *what*, and the *impact*) so you can trim it down and tailor it per application. Cut the parenthetical/context clauses for a tighter one-page version.

---

## Summary

Software engineer with 4+ years spanning test automation, QA, and full-stack development across three enterprise platforms in a regulated domain. Track record of large-scale framework modernization (Java 8 → 17, Spring 5 → 6, Hibernate, Jakarta EE), building resilient cloud-integrated services, and delivering robust BDD/regression automation for high-volume systems. Comfortable owning work end to end: from application-security remediation and CI/CD pipeline integration to production bug fixes and release preparation.

---

## Core Skills

- **Languages:** Java, JavaScript/Node.js, Python, SQL
- **Frameworks:** Spring / Spring Boot, Hibernate, Struts, JUnit 4/5, Mockito, EasyMock
- **Cloud & Infra:** AWS (S3, SQS, SNS, SES, Lambda, RDS), Docker, Tomcat, Ansible
- **CI/CD & Quality:** Jenkins, SonarQube, Maven, JaCoCo, application security logging
- **Testing:** BDD/regression automation, GraphQL API testing, integration testing, agentic unit testing

---

## Experience

### Developer — Exam Authoring & Test-Delivery Platform
*2025 – Present*

Full-stack developer on a large exam-authoring and test-delivery platform, working across 60+ services and driving an org-wide Java modernization effort.

- **Led the Java 17 / Spring 6 modernization** of several core legacy applications. *Context:* these apps were on Java 8 with Spring 5, Struts 2, and older Hibernate, blocking security patches and newer library support. *Work:* upgraded to Java 17, Spring 6.2, Hibernate 6, Struts 7, Tomcat 10, and Jakarta EE 10, including the full javax → jakarta namespace migration. *Impact:* unblocked the platform's long-term support path and kept full test suites green through the migration.
- **Upgraded the test tooling that the migration depended on.** *Context:* the legacy test stack (JUnit 4, Mockito 4, EasyMock 2.5) was incompatible with Java 17's module system and byte-buddy requirements. *Work:* migrated to JUnit 5 (Jupiter, with vintage engine for gradual cutover), Mockito 5.14, and EasyMock 5.4, and added `--add-opens` reflection config. *Impact:* re-enabled previously excluded security tests (CSRF, XSS, input sanitizer) and unblocked CI.
- **Built real, mock-free integration test coverage to prove upgrade readiness.** *Context:* the apps had thin, mock-heavy coverage that couldn't validate behavior against a real database on the new stack. *Work:* added hundreds of integration tests (Hibernate ORM CRUD, HQL, named queries, lazy loading, `@ManyToOne` relationships, transaction commit/rollback, JDBC CRUD) running on embedded H2. *Impact:* e.g., 217 tests passing on one core application post-upgrade, giving confidence to ship the migration.
- **Modernized cloud integration and transaction handling.** *Context:* code used the deprecated AWS SDK v1 and manual/legacy transaction patterns incompatible with Spring 6. *Work:* migrated email messaging from AWS SDK v1 → v2 and converted legacy DAOs to Spring-managed transactions. *Impact:* removed a deprecated dependency and aligned data access with the framework's transaction model.
- **Implemented retry logic for slow upstream report retrieval.** *Context:* a service pulled reports from an external system that were sometimes slow to generate, with no retry — causing missed/failed fetches. *Work:* added retry logic with tuned sleep intervals and traceability logging of pending request IDs after max retries. *Impact:* reduced failed fetches and made next-cycle debugging possible.
- **Fixed bulk-report email delivery broken by the Java 17 upgrade.** *Context:* the upgrade broke bulk-report emails and left logging fragmented across environments. *Work:* consolidated log4j config, migrated to the slf4j2 bridge, fixed access/exception/trace log routing, and resolved a Tomcat 10 context-path issue. *Impact:* restored bulk reporting and made dev/QA logs usable again.
- **Standardized ISO 8601 timestamp logging for centralized log search in Node.js services.** *Context:* log timestamps were in Zulu/UTC without local time or millisecond precision, hurting log correlation. *Work:* implemented a local-timezone ISO 8601 formatter with millisecond accuracy per the logging standard. *Impact:* improved log searchability and cross-service correlation.
- **Integrated SonarQube scanning into CI pipelines for Node.js Lambdas.** *Context:* Node Lambda projects had no static-analysis gate in CI. *Work:* added a SonarQube Jenkins stage, fixed PIP-detection timeouts on Node packages, pinned Node 22, and corrected project-key mapping to app name. *Impact:* brought Lambda code under the same quality/security gate as the rest of the platform.
- **Remediated a security finding — unchecked Spring autobinding.** *Context:* an unrestricted request-to-object binding created a mass-assignment risk. *Work:* constrained autobinding on the affected endpoints. *Impact:* closed the vulnerability.
- **Built test-result publishing automation into the issue tracker.** *Context:* automation suites weren't reliably publishing results, and credentials were inconsistent across suites. *Work:* standardized the publisher configuration and tagged feature files by component. *Impact:* consistent, traceable test reporting.
- **Upgraded the build toolchain.** *Context:* older Maven and plugin versions were incompatible with the Java 17 build. *Work:* upgraded Maven to 3.9.2 and associated plugins, including JaCoCo 0.8.13. *Impact:* enabled reliable builds and coverage reporting on the new stack.

### QA & Developer — Learning Marketplace Platform
*2025*

Delivered backend features, integrations, and security remediation for a learning marketplace platform (backend APIs, serverless Lambdas, front-end micro-app).

- **Built LMS account provisioning after bulk user upload.** *Context:* users uploaded in bulk needed corresponding LMS accounts created automatically. *Work:* implemented the account-creation flow and the supporting configuration and DB schema changes. *Impact:* automated a previously manual onboarding step.
- **Developed an internal file-upload utility API.** *Context:* internal services lacked a reusable way to push files to object storage. *Work:* built a dedicated S3 upload API for internal use. *Impact:* gave other components a consistent file-upload path.
- **Implemented save-terms-and-conditions-as-PDF in the front-end micro-app.** *Context:* users needed a durable PDF record of accepted terms. *Work:* built the PDF generation/save feature (iterated to a V2) and updated the terms document. *Impact:* produced an auditable record of consent.
@                         
