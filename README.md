![gophers](https://raw.githubusercontent.com/ashleymcnamara/gophers/master/GOPHER_AVATARS.jpg)

# BEW 2.5: Patterns & Practices in Strongly Typed Languages

<!-- omit in toc -->
### Table of Contents

1. [Course Description](#course-description)
1. [Prerequisites](#prerequisites)
1. [Course Specifics](#course-specifics)
1. [Learning Objectives](#learning-objectives)
1. [Schedule](#schedule)
1. [Course Deliverables](#course-deliverables)
1. [Late Assignment Policy](#late-assignment-policy)
1. [Evaluation](#evaluation)
1. [Additional Resources](#additional-resources)
1. [Information Resources](#information-resources)
1. [Make School Course Policies](#make-school-course-policies)

## Course Description

_In this course, students discover the value of strongly typed languages in server-side architectures, and dive deep into performant, concurrent programming paradigms present in Go. In studying Go, which is known for its ability to blend the expressive features of dynamic languages (Python, JavaScript) with the performance capabilities of compiled languages (C, C++), students will gain the syntactic diversity required in today's large-scale platform engineering pursuits. Throughout the course, students will learn and implement the design patterns and best practices that make Go a top choice at high-velocity startups like Lyft, Heroku, Docker, and Medium._

## Prerequisites

- [BEW 1.1](https://make.sc/bew1.1)
- [BEW 1.2](https://make.sc/bew1.2)

## Course Specifics

**Course Delivery**: online | 7 weeks | 14 sessions

**Course Credits**: 3 units | 37.5 Seat Hours | 75 Total Hours

## Learning Objectives

1. Design and implement command line interfaces, APIs, and bots in Go.
2. Identify and describe the architectures wherein the features of Golang could be best utilized.
3. Build data structures that support unmarshalling JSON retrieved from third-party APIs.
4. Apply Object Relational Mapping techniques to persist data to relational databases in Go.
5. Examine benchmarks to determine how to improve the speed and readability of a Golang project.
6. Gain experience deploying APIs and bots to production.

## Schedule

| Class | Date        | Topics                                                                                                        |
| :---: | ----------- | ------------------------------------------------------------------------------------------------------------- |
|   -   | Tue, Jan 19 | **No Class - MLK Day**                                                                                        |
|   1   | Thu, Jan 21 | [**Intro to Go / Tutorial Launch**](https://tour.golang.org)<br>🔬**Lab**: [Tutorial](https://tour.golang.org) |
|   2   | Tue, Jan 26 | **[Static Site Generators](Lessons/SSGProject.md)**<br> 🔬**Lab**: SSG MVP                                     |
|   3   | Thu, Jan 28 | **[Files & Directories](Lessons/FilesDirectories.md)**                                                        |
|   4   | Tue, Feb 2  | **[Introducing Warmups](Lessons/WarmUps.md)**: 1<sup>st</sup>Daily Drill <br>🔬**Lab**: SSG MVP / SSG v1.1     |
|   5   | Thu, Feb 4  | **[Fast Functionality via 3rd Party Libraries](Lessons/3rdPartyLibs.md)**                                     |
|   6   | Tue, Feb 9  | 🔬**Lab**: SSG v1.2                                                                                            |
|   7   | Thu, Feb 11 | **[Scraping the Web](Lessons/WebScraping.md)**<br>**[Working With JSON](Lessons/JSON.md)**                    |
|   8   | Tue, Feb 16 | 🔬**Lab**: Web Scraper                                                                                         |
|   9   | Thu, Feb 18 | [Project Kickoff](Project/MakeUtility.md)                                                                     |
|  10   | Tue, Feb 23 | **[Concurrency & Goroutines](Lessons/Lesson07.md)**                                                           |
|  11   | Thu, Feb 25 | **[Benchmarking & Testing](Lessons/Lesson09.md)**<br>🔬**Lab**: Final Project                                  |
|  12   | Tue, Mar 2  | **[Documentation & Deployments](Lessons/DocsDeploy.md)**<br>🔬**Lab**: Final Project                           |
|  13   | Tue, Mar 4  | [**Final Presentations**](Project/MakeUtility.md)                                                             |

## Course Deliverables

We will be using Gradescope this term, which allows us to provide fast and accurate feedback on your work. All assigned work will be submitted through Gradescope, and assignment and exam grades will be returned through Gradescope. As soon as grades are posted, you will be notified immediately so that you can log in and see your feedback. You may also submit regrade requests if you feel we have made a mistake.

Your Gradescope login is your Make School email, and your password can be changed at https://gradescope.com/reset_password. The same link can be used if you need to set your password for the first time.

*Assignments **must** be submitted to Gradescope by **11:59PM PST** on the date due.*

| 📚   Assignment                                      | 🔗   Criteria                                                                                                                                                                         | 📆   Due Date                                                                                     |
| :-------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| **[Tour of Go](https://tour.golang.org/welcome/1)** | Done in Class                                                                                                                                                                        | January 23, 2020 *(Thursday)*                                                                    |
| **Static Site Generator**                           | [MVP](https://github.com/Make-School-Labs/makesite#mvp)  <br />[v1.1](https://github.com/Make-School-Labs/makesite#v1.1) / [v1.2](https://github.com/Make-School-Labs/makesite#v1.2) | <u>MVP</u>: Feb 02, 2020 *(Tuesday)*<br /><u>v1.1</u> / <u>v1.2</u>: Feb 11, 2020 *(Thursday)* |
| **Web Scraper**                                     | [Requirements](https://make.sc/makescraper)                                                                                                                                          | Feb 23, 2020 (*Tuesday*)                                                                          |
| **Blog Post**                                       | [Rubric](https://docs.google.com/document/d/1T1oqHFoRo0kl7mPUTFupmsoEkLYltKsVgtqyGKDaCgY/edit)                                                                                       | March 4, 2020 *(Tuesday)*                                                                         |
| **MakeUtility Project <br>& Presentation**                             | [Requirements](https://make.sc/makeutility)                                                                                                                                          | March 4, 2020 *(Tuesday)*                                                                                   |

## Late Assignment Policy

- Late assignments that are submitted **more than 5 days (120 hours)** after the deadline will be given a **25% late penalty**.
- The **absolute last day** to submit any assignment will be **Tuesday, March 4 at 11:59 PM**.

If you require accommodations or have extenuating circumstances such as prolonged illness, please contact your instructor to request an extension.

## Evaluation

**To pass this course you must meet the following requirements**:

- Complete the [tutorial](#tutorial), deliverables, [final project](#final-project), and [final presentation](#final-presentation) as assigned in class and described in the sections below.
- Actively participate in class and abide by the attendance policy.
- Make up all classwork from all absences.

<!-- omit in toc -->
### Tutorial

Complete the [tutorial](https://tour.golang.org) assigned in class; assessed via graded warmup during week two.

<!-- omit in toc -->
### Blog Post

Demonstrate confidence writing and speaking about Go topics by writing a 500+ blog post on a language feature of your choice.

Your blog post must be accessible to the general public to earn credit; do not submit draft posts.

Your grade will be determined via the [Make School Blog Post Rubric](https://docs.google.com/document/d/1T1oqHFoRo0kl7mPUTFupmsoEkLYltKsVgtqyGKDaCgY/edit). **You must earn a score of 2.5 or higher to pass**.

<!-- omit in toc -->
### Final Project

Complete the final project according to the associated [project rubric](Project/MakeUtility.md).

<!-- omit in toc -->
### Final Presentation

The delivery of a live or pre-recorded presentation is required to pass this course. **Presentations will be delivered on Wednesday, December 9th on our final day of class**.

Your **three to five minute presentation** should focus on the **experience you gained** and **lessons you learned** while implementing one of the three [Challenges](#challenges) in this course.

**Your final presentation will be evaluated based on the [Make School Presentation Rubric](https://docs.google.com/document/d/1WTLcZNyvRGYDz5L8Kr8a0ILbFAyr92u85paoqGFjxPg/edit). You must earn an average of 2.5 on the rubric to pass**.

## Additional Resources

<!-- omit in toc -->
### Update to Latest Version of Go

New version of Go released? No problem! Run the following command to install the latest version of Golang on your Mac or Linux system:

```bash
git clone https://github.com/udhos/update-golang
cd update-golang
sudo ./update-golang.sh
```

<!-- omit in toc -->
### Links

- [make.sc/library](http://make.sc/library)
- [Gophercises](https://gophercises.com/): Real-world side projects with video tutorials!
- [TutorialEdge - Golang Repository](https://github.com/elliotforbes/tutorialedge-v2/tree/master/content/golang): Mini-tutorials to introduce and enhance your Golang knowledge.
- [YouTube - Todd Mcleod](https://www.youtube.com/user/toddmcleod/playlists): Videos to reinforce Golang concepts and techniques that we cover in class.
- [Echo Framework](https://echo.labstack.com/guide): Documentation for Echo, a high performance, extensible, minimalist Go web framework.
- [GORM](http://doc.gorm.io/#): The fantastic ORM library for Golang.

## Information Resources

Any additional resources you may need (online books, etc.) can be found here. You can also find additional resources through the library linked below:

- [make.sc/library](http://make.sc/library)

## Make School Course Policies

- [Program Learning Outcomes](https://make.sc/program-learning-outcomes) - What you will achieve after finishing Make School, all courses are designed around these outcomes.
- [Grading System](https://make.sc/grading-system) - How grading is done at Make School
- [Diversity and Inclusion Statement](https://make.sc/diversity-and-inclusion-statement) - Learn about Diversity and Inclusion at Make School
- [Academic Honesty](https://make.sc/academic-honesty-policy) - Our policies around plagiarism, cheating, and other forms of academic misconduct
- [Attendance Policy](https://make.sc/attendance-policy) - What we expect from you in terms of attendance for all classes at Make School
- [Course Credit Policy](https://make.sc/course-credit-policy) - Our policy for how you obtain credit for your courses
- [Disability Services (Academic Accommodations)](https://make.sc/disability-services) - Services and accommodations we provide for students
- [Online Learning Tutorial](https://make.sc/online-learning-tutorial) - How to succeed in online learning at Make School
- [Student Handbook](https://make.sc/student-handbook) - Guidelines, policies, and resources for all Make School students
