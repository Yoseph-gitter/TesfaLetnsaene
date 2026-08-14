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
