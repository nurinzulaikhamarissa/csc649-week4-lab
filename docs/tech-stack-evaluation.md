# Tech Stack Evaluation

## Project
MeritMatch: An Intelligent Multi-Criteria Decision System for University Merit Programme Recommendation

MeritMatch is a web-based system that helps university students discover and rank merit-eligible programmes based on their preferences, location, schedule, and merit-point requirements.

## Requirements that drive the decision
- FR-01: The system shall allow students to browse and search for university merit programmes using criteria such as programme name, organiser, location, date, and merit points.

- FR-02: The system shall filter programmes according to students' preferences and constraints, including location and schedule.

- FR-03: The system shall rank suitable programmes using Weighted Scoring and TOPSIS to provide personalised recommendations.

- NFR-01: The system shall provide a simple, user-friendly interface that students can navigate easily.

- NFR-02: The system shall use cost-effective development tools and hosting services suitable for a student FYP, with reasonable response times and secure handling of user data.

## Options
- Option A: HTML, CSS, JavaScript, and Firebase for a web application with cloud database services.

- Option B: Python Flask, HTML, CSS, JavaScript, Bootstrap, and a relational database (SQLite for development, with MySQL as a possible deployment option).

- Option C: Laravel, PHP, MySQL, HTML, CSS, JavaScript, and Bootstrap for a full-stack web application.

## Decision matrix
Weight: how important the criterion is for YOUR project (1 = low, 5 = high).
Score: how well each option does (1 = poor, 5 = excellent).
Weighted score = weight x score. Add them up for each option.

| Criterion                          | Weight  | A score  | B score  | C score  |
|------------------------------------|---------|----------|----------|----------|
| Fits my requirements               |    5    |    3     |    5     |    4     |
| Skills I already have              |    3    |    4     |    3     |    2     |
| Time to build before my deadline   |    5    |    5     |    4     |    3     |
| Free hosting and tools             |    4    |    4     |    4     |    4     |
| Performance and security needs     |    3    |    3     |    4     |    4     |
| Room to grow later                 |    3    |    3     |    4     |    5     |
| **Total (weighted)**               |         |    83    |   94     |    84    |

## Decision record
- **Context:** MeritMatch requires a web application that can manage university merit programmes, apply multiple constraints, and rank suitable programmes using Weighted Scoring and TOPSIS. Development time and budget are limited, so the technology stack should be practical, affordable, and maintainable.
- **Decision:** Choose Option B: Python Flask with HTML, CSS, JavaScript, Bootstrap, and a relational database.
- **Reasons:** 
1. Algorithm compatibility: Python is suitable for implementing rule-based constraint filtering, Weighted Scoring, and TOPSIS without requiring a separate algorithm service.

2. Development feasibility: Flask provides the essential web application functionality without the overhead of a larger framework, making it suitable for a student FYP.

3. Cost and flexibility: Python and Flask are open-source, and the application can begin with SQLite before moving to MySQL if the deployment or data requirements justify it.
- **Consequences:** 
What becomes easy: Implementing recommendation calculations, testing ranking results, connecting the recommendation logic to the web interface, and updating the system as requirements change.

What becomes hard: Building authentication, access control, database management, and deployment requires additional configuration and testing. Flask does not provide every feature automatically, so these must be implemented carefully.
- **Risks and next review:** 
- Free hosting providers may impose usage limits, sleep periods, or other restrictions.

- Incorrect weights or poorly defined criteria could produce unsuitable programme rankings.

- The database design may need changes as programme information and student requirements expand.

- Review this decision after completing the system requirements and database design, and again after implementing the first working recommendation prototype. Validate the ranking calculations using sample programmes and manually checked results before final evaluation.
