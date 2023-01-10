<template>


  <!-- Landing Page -->
  <section>
    <div class="top-container container-fluid">
      <img class="astronaut img-fluid" src="https://i.postimg.cc/qBmNgHdx/astronaut.png" alt="astronaut">
      <h1 class="text-black">Hey, I'm Javier Goodall</h1>
      <p class="subheading text-black">Aspiring Full Stack Web Developer</p>
      <img class="spaceship img-fluid" src="https://i.postimg.cc/0yHgJZy3/startup.png" alt="spaceship">
      <img class="moon img-fluid" src="https://i.postimg.cc/PJYBwkRr/halfmoon.png" alt="moon">
      <a href="#" class="link-arrow"><img src="https://i.postimg.cc/mkLJ7tnZ/up-arrow.png" loading="lazy"
        alt="scroll button" class="arrow">
      </a>
    </div>
  </section>


  <!-- ABOUT ME -->
  <section id="about">
    <div class="container-fluid row">
      <h3 class="display-3 text-black text-md-center mb-5 mt-3">About Me</h3>
      <div class="about col-md-6">
        <img class="profile1 my-3 img-fluid mx-4 w-75 float-md-end" src="https://i.postimg.cc/7ZBQDZDk/Profile
        Me.jpg" alt="Javier Profile">
      </div>
      <div class="col-md-6 text-md-start lh-lg mt-5 text-black">
        <p class="paragraph">I'm currently enrolled at Life Choices Academy, where I'm learning technical and soft
          skills to become a full stack developer. Coding has changed my life because it has provided me with
          problem-solving skills and a way to communicate with others on a technical level. Furthermore, I enjoy
          designing pages where I can truly provide users with pleasurable interactions and experiences. Life
          Choices Academy has helped to boost my self-esteem and kept me motivated throughout the whole journey.
          Since I started coding I noticed that I can never be bored because there is always something new to learn
        </p>
      </div>
    </div>
  </section>


  <!-- Resume -->
  <div id="resume" class="container-fluid text-black">
    <h3 class="fw-bold display-3 text-black mt-5 mb-3 text-decoration-underline">Resume</h3>
    <h3 class="fw-bold">Education</h3>
    <ul class="resume lh-lg me-4">
      <li v-for="degree in education" :key="degree.id">
        {{ degree.startDate }} - {{ degree.endDate }}
        <p>{{ degree.degree }} - {{ degree.institution }}</p>
        <p>{{ degree.description }}</p>
      </li>
    </ul>
  </div>

  <!-- Experience -->
  <div id="skills" class="container-fluid text-black">
    <h3 class="fw-bold">Experience</h3>
      <ul class="lh-lg me-4">
        <li v-for="job in experience" :key="job.id">
          {{ job.startDate }} - {{ job.endDate }}
          <p>{{ job.title }} - {{ job.company }}</p>
        </li>
      </ul>
  </div>

    <!-- Skills -->
    <div id="skills" class="container-fluid text-black">
    <h3 class="text-left fw-bold mt-3 mb-4">My Skills</h3>
    <div class="progressbar m-auto">
      <div v-for="skill in skills" :key="skill.name">
        <h3>{{ skill.name }} <i :class="'fa-brands ' + skill.icon"></i></h3>
        <div class="progress my-3 w-75">
          <div :class="'progress-bar bg-black'" role="progressbar" :style="{width: skill.percentage + '%'}">{{
            skill.percentage }}%
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  // The watch property will look for changes on the $route property and perform the actions when it changes.
  // For this example when the route's hash fragment is #about, it will use the 
  //  document.getElementById("about")method to find the element with the id "about" and call the scrollIntoView().
  watch: {
  $route() {
    if (this.$route.hash === "#about") {
      document.getElementById("about").scrollIntoView({ behavior: "smooth", block: "start" });
    }
    if (this.$route.hash === "#resume") {
      document.getElementById("resume").scrollIntoView({ behavior: "smooth", block: "start" });
  }
}
},


// Education
data() {
    return {
        education: [
        {
            id: 1,
            degree: 'Bachelor Pass',
            institution: 'Plumstead High School',
            startDate: 'January 2013',
            endDate: 'December 2017',
            description: ''
        },
        {
            id: 2,
            degree: 'Bachelor of Arts',
            institution: 'University of Cape Town',
            startDate: 'February 2019',
            endDate: 'October 2022',
            description: 'Majored in Religious Studies, Industrial Psychology & Film Studies'
        },
        {
            id: 3,
            degree: 'Web Development Certificate',
            institution: 'Life Choices Academy',
            startDate: 'September 2022',
            endDate: 'Present',
            description: '',
        }
        ],

        // Experience
      experience: [
        {
          startDate: 'February 2019',
          endDate: 'February 2020',
          title: 'Volunteer',
          company: 'Students Health and Welfare Centre Organization (SHAWCO)',
        },
        {
          startDate: 'January 2021',
          endDate: 'Present',
          title: 'Film and Television Extra',
          company: '39 Steps',
        },
      ],

      // Skills
      skills: [
      {
          name: 'HTML',
          percentage: 85,
          icon: 'fa-html5'
        },
        {
          name: 'CSS',
          percentage: 70,
          icon: 'fa-css3-alt'
        },
        {
          name: 'Bootstrap',
          percentage: 75,
          icon: 'fa-bootstrap'
        },
        {
          name: 'Javascript',
          percentage: 60,
          icon: 'fa-js'
        },
        {
          name: 'Vue.js',
          percentage: 70,
          icon: 'fa-brands fa-vuejs'
        }
      ]
    }
}

}
</script>


<style scoped>
h1 {
    font-size: 50px;
    font-family:'Cinzel', serif;
    animation: fadeIn 5s; 
}
.subheading {
    animation: fadeIn 10s;
}
@keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 3; }
  }
.link-arrow {
    position: fixed;
    bottom: 0.5em;
    right: 0.3em;
}
.arrow {
    width: 40px;
    background-color: white;
}
/* Containers */
.top-container {
    background-color: rgb(82, 97, 107);
    position: relative;
    padding-top: 230px;
}
.telescope {
    width: 100px;
    height: 150px;
    margin: 20px;
}
.skills2 {
    width: 250px;
    height: 300px;
    border-radius: 10%; 
}
/* IMAGES */
.astronaut {
    position: absolute;
    width: 90px;
    height: 80px;
    right: 300px;
    top: 50px;
    
    /* Hover */
    -webkit-animation: mover 2s infinite  alternate;
    animation: mover 2s infinite  alternate;
  }
  @-webkit-keyframes mover {
    0% { transform: translateY(0);
     }
     100% { transform: translateY(-20px); 
    }
  }
  @keyframes mover {
     0% { transform: translateY(0); 
    }
    100% { transform: translateY(-20px); 
    }
  }
.spaceship {
    position: absolute;
    width: 90px;
    height: 80px;
    left: 300px;
    bottom: 300px;

    /* Hover */
    -webkit-animation: mover 2s infinite  alternate;
    animation: mover 2s infinite  alternate;
  }
    @-webkit-keyframes mover {
    0% { transform: translateY(0);
     }
     100% { transform: translateY(-20px); 
    }
  }
  @keyframes mover {
     0% { transform: translateY(0); 
    }
    100% { transform: translateY(-20px); 
    }
  }
.profile1 {
    box-shadow: 0 0 20px 7px black;
}




/* SKILLS */
ul {
    list-style-type: none;
}
.progress {
    margin: auto;
    height: 30px;
}
/* Projects */
.project {
    width: 100px;
    height: 150px;
}
  

/* MEDIA QUERY */

@media screen  and (max-width:1080px) {
    h1  {
        font-size: xx-large;
        padding-top: 80px;
    }
    .logo {
        width: 3rem;
        height: 3rem;
    }
    .subheading {
        font-size: small;
        padding-bottom: 80px;
    }
    p {
        font-size: small;
        text-align: center;
    }
    .paragraph {
        margin-right: 30px;
        margin-left: 50px;
    }
    .top-container {
        padding-top: 150px;
    }
    h3 {
        font-size: medium;
    }
    li {
        font-size: small;
        margin: auto;
    }
    body {
        text-align: center;
    }
    .moon {
        width: 400px;
    }
    .astronaut {
        top: 100px;
        right: 50px;
        width: 50px;
        height: 50px;
    }
    .spaceship {
        top: 150px;
        left: 50px;
        width: 50px;
        height: 50px;
    }   
    .footer i {
        font-size: small;
    }
    .footer a {
        font-size: small;
        line-height: 36px;
    }
    .person {
        width: 150px;
        height: 150px;
        max-width: 100%;
    }
    .arrow {
        width: 30px;
    }
}

</style>
