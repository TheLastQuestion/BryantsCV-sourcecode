// src="./assets/headshot.jpg"

<template>
  <div class="main-wrapper">
    <head>
      <link href="https://fonts.googleapis.com/css?family=Saira+Extra+Condensed:100,200,300,400,500,600,700,800,900" rel="stylesheet">
      <link href="https://fonts.googleapis.com/css?family=Open+Sans:300,300i,400,400i,600,600i,700,700i,800,800i" rel="stylesheet">
    </head>
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none">Start Bootstrap</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="./assets/headshot.jpg" alt="">
        </span>
      </a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Education</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#publications">Publications</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Skills</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">Interests</a>
          </li>
          <!-- <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#awards">Awards</a>
          </li> -->
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">

      <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <h1 class="mb-0">{{ name }}
            <span class="text-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">{{ address }}
            <a href="mailto:bryant.d.renaud@gmail.com">{{ email }}</a>
          </div>
          <p class="mb-5">{{ aboutMe }}</p>
          <ul class="list-inline list-social-icons mb-0">
            <!-- <li class="list-inline-item">
              <a href="#">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-facebook fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li> -->
            <li class="list-inline-item">
              <a target=_blank href="https://twitter.com/bryant_renaud">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-twitter fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a target=_blank href="https://www.linkedin.com/in/bryantrenaud">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-linkedin fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a target=_blank href="https://github.com/TheLastQuestion">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
          <h2 class="mb-5">Experience</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="job in experience" :key="job.description">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ job.position }}</h3>
              <div class="subheading mb-3">{{ job.company }}</div>
              <p><span v-html="job.description"></span></p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
            </div>
          </div>

        </div>

      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="education">
        <div class="my-auto">
          <h2 class="mb-5">Education</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="school in education" :key="school.institution">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ school.institution }}</h3>
              <div class="subheading mb-3">{{ school.degree }}</div>
              <p><span v-html="school.description"></span></p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">Conferred: {{ school.conferred }}</span>
            </div>
          </div>

          <h3 class="mb-0">Other Training</h3>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
             Human-Centered Design</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Systems Thinking</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Agile Project Management</li>
          </ul>

        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="publications">
        <div class="my-auto">
          <h2 class="mb-5">Publications</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5" v-for="publication in publications" :key="publication.title">
            <div class="resume-content mr-auto">
              <h3 class="mb-0"><span v-html="publication.title"></span></h3>
              <div class="subheading mb-3">{{ publication.publisher }}</div>
              <p><span v-html="publication.description"></span></p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">Published: {{ publication.date }}</span>
            </div>
          </div>

        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">Skills</h2>

          <div class="subheading mb-3">Languages</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
              Advanced Spanish</li>
          </ul>
          <div class="subheading mb-3"></div>
          <div class="subheading mb-3">Software</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
             JavaScript</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              R</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Stata</li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Adobe Premiere</li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="interests">
        <div class="my-auto">
          <h2 class="mb-5">Interests</h2>
          <p>I like to design and make things in my spare time. This often means fiddling around with my 3d printer, CAD software, and hobby electronics.</p>
          <p class="mb-0">I love science fiction novels and like to stay up to speed with the latest developments in human-centered design, especially as applied to digital services.</p>
        </div>
      </section>

    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'Bryant Renaud',
      name: 'BRYANT',
      surname: 'RENAUD',
      address: 'Washington DC ·',
      email: 'bryant.d.renaud@gmail.com',
      aboutMe: 'I work as a strategist at the meeting point between digital services and organizational design. Questions involving planning and operations of digital service providers keep me up at night and get me out of bed in the morning. Current areas of interest include: data governance, IT portfolio management, and connecting concepts of cybersecurity risk with other enterprise risk considerations.',
      experience: [
        {
          position: 'Presidential Management Fellow',
          company: 'White House Office of the Federal Chief Information Officer',
          description: 'Develop IT- and data-management policy, as well as technical guidance for Federal agencies. Assess IT portfolio management at NASA and US Army Corps of Engineers using key performance indicators and dashboards. Brief senior leadership on status of IT and data management in Federal government.',
          startDate: 'June 2016',
          endDate: 'Present'
        },
        {
          position: 'Policy Advisor',
          company: 'State Department, Office of the Coordinator for Cyber Issues',
          description: 'Developed cybersecurity talking points for senior officials’ use in bilaterals and multilaterals. Work with US diplomats abroad to support engagements and demarche foreign governments. Oversaw projects executed by MITRE and the Software Engineering Institute.',
          startDate: 'May 2017',
          endDate: 'October 2017'
        },
        {
          position: 'Researcher',
          company: 'Harvard Innovation Partnership',
          description: 'Worked with a team of mayors, professors and students to help 5 cities (Fitchburg, Lawrence, Winthrop, Salem, Chelsea) develop <a target=_blank href="http://ash.harvard.edu/news/experiencing-innovation">data-driven performance management</a>. Consulted cities on operations and implementing PerformanceStat model. Oversaw development of web application for city administration and data integration.',
          startDate: 'November 2014',
          endDate: 'May 2016'
        },
        {
          position: 'Policy Fellow',
          company: 'Oregon Governor\'s Natural Resources Office',
          description: 'Contributed to Governor’s positions on wildfire suppression and water quality policy.',
          startDate: 'June 2015',
          endDate: 'August 2015'
        },
        {
          position: 'Senior Research Assistant',
          company: 'Brookings Institution',
          description: 'Wrote <a href="#publications">policy briefs</a> on topics related to US fiscal outlook, retirement, savings and health care.',
          startDate: 'November 2012',
          endDate: 'August 2014'
        },
        {
          position: 'Research Fellow',
          company: 'Economic Policy Research Institute',
          description: 'Managed teams of 10+ interns from countries in Africa, Europe, and the US. Conducted statistical analyses and micro-simulations using datasets of 11 million records. Taught courses on international policy design and micro-simulation for policy-makers and Master’s students in Ethiopia, Kenya, Netherlands, South Africa, Thailand, and Zimbabwe.',
          startDate: 'November 2012',
          endDate: 'August 2014'
        }
      ],
      education: [
        {
          institution: 'Harvard Kennedy School of Government',
          degree: 'Master of Public Policy',
          description: 'Capstone: <a href="http://bryantrenaud.com/boston-311">Using Data Science to Promote Equity in Boston’s 311 System</a>',
          link: 'http://bryantrenaud.com/boston-311',
          conferred: '2016'
        },
        {
          institution: 'Williams College',
          degree: 'Bachelor of Arts in Polical Economy with Honors',
          description: null,
          link: null,
          conferred: '2011'
        }
      ],
      publications: [
        {
          title: '<a target=_blank href="http://www.urban.org/sites/default/files/alfresco/publication-pdfs/413123-Student-Loans-Rising.PDF">Student Loans Rising: An Overview of Causes, Consequences, and Policy Options</a>',
          publisher: 'Brookings Institution',
          description: 'Borrowing to finance higher education has increased markedly over the past two decades. These trends are associated with a variety of negative economic outcomes for households who hold the debt, but those outcomes must be weighed against the net increase in earnings the households receive from acquiring more education.',
          date: '2014'
        },
        {
          title: '<a target=_blank href="https://www.unicef.org/evaldatabase/files/The_South_African_Child_Support_Grant_Impact_Assessment.pdf">South African Child Support Grant Impact Assessment: Evidence from a Survey of Children, Adolescents and their Households.</a>',
          publisher: 'Economic Policy Research Institute',
          description: 'The Child Support Grant (CSG) is an important instrument of social protection in South Africa, reaching over 10 million South African children each month. This report presents the findings of a research team’s analysis of a specially designed survey fielded in rural and urban areas of five South African provinces, supporting the rigorous impact assessment of how access to the CSG affects key aspects of child and adolescent well-being.',
          date: '2012'
        }
      ]
    }
  },
  mounted () {
    const $ = this.jquery
    this.$nextTick(() => {
      // our custom jQuery code goes here
      $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function () {
        if (location.pathname.replace(/^\//, '') === this.pathname.replace(/^\//, '') && location.hostname === this.hostname) {
          var target = $(this.hash)
          target = target.length ? target : $('[name=' + this.hash.slice(1) + ']')
          if (target.length) {
            $('html, body').animate({
              scrollTop: (target.offset().top)
            }, 1000, 'easeInOutExpo')
            return false
          }
        }
      })
      // Closes responsive menu when a scroll trigger link is clicked
      $('.js-scroll-trigger').click(function () {
        $('.navbar-collapse').collapse('hide')
      })
      // Activate scrollspy to add active class to navbar items on scroll
      $('body').scrollspy({
        target: '#sideNav'
      })
    })
  }
}
</script>

<style>
body {
  font-family: 'Open Sans', serif;
  padding-top: 54px;
  color: #868e96;
}

@media (min-width: 992px) {
  body {
    padding-top: 0;
    padding-left: 17rem;
  }
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Saira Extra Condensed', serif;
  font-weight: 700;
  text-transform: uppercase;
  color: #343a40;
}

h1 {
  font-size: 6rem;
  line-height: 5.5rem;
}

h2 {
  font-size: 3.5rem;
}

.subheading {
  text-transform: uppercase;
  font-weight: 500;
  font-family: 'Saira Extra Condensed', serif;
  font-size: 1.35rem;
}

.list-social-icons a {
  color: #495057;
}

.list-social-icons a:hover {
  color: #6da8db;
}

.list-social-icons a .fa-lg {
  font-size: 1.75rem;
}

.list-icons {
  font-size: 3rem;
}

.list-icons .list-inline-item i:hover {
  color: #cde2f4;
}

#sideNav .navbar-nav .nav-item .nav-link {
  font-weight: 600;
  text-transform: uppercase;
}

@media (min-width: 992px) {
  #sideNav {
    text-align: center;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    width: 17rem;
    height: 100vh;
  }
  #sideNav .navbar-brand {
    display: flex;
    margin: auto auto 0;
    padding: 0.5rem;
  }
  #sideNav .navbar-brand .img-profile {
    max-width: 10rem;
    max-height: 10rem;
    border: 0.5rem solid rgb(109,168,219);
  }
  #sideNav .navbar-collapse {
    display: flex;
    align-items: flex-start;
    flex-grow: 0;
    width: 100%;
    margin-bottom: auto;
  }
  #sideNav .navbar-collapse .navbar-nav {
    flex-direction: column;
    width: 100%;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item {
    display: block;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item .nav-link {
    display: block;
  }
}

section.resume-section {
  border-bottom: 1px solid #dee2e6;
  padding-top: 5rem !important;
  padding-bottom: 5rem !important;
}

section.resume-section .resume-item .resume-date {
  min-width: none;
}

@media (min-width: 768px) {
  section.resume-section {
    min-height: 100vh;
  }
  section.resume-section .resume-item .resume-date {
    min-width: 18rem;
  }
}

@media (min-width: 992px) {
  section.resume-section {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }
}

.bg-primary {
  background-color: #015aab !important;
}

.text-primary {
  color: #015aab !important;
}

a {
  color: #015aab;
}

a:hover, a:focus, a:active {
  color: #6da8db;
}
</style>
