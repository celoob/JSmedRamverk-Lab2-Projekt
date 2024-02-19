<script>
import TagItem from './TagItem.vue'

export default {
  components: {
    TagItem
  },
  data() {
    return {
      projects: [],
      searchInput: '',
      tags: ['Logo', 'Website', 'Freelance', 'University', 'Fun']
    }
  },
  mounted() {
    this.fetchProjects()
  },
  methods: {
    // hämta data från json
    async fetchProjects() {
      try {
        const response = await fetch('data.json')
        const data = await response.json()
        this.projects = data
      } catch (error) {
        console.error('Error fetching projects:', error)
      }
    },
    // sök med tags
    addTagToSearch(tag) {
      this.searchInput = tag
    }
  },
  computed: {
    // filtrering
    filteredProjects() {
      return this.projects.filter((project) =>
        project.tags.toLowerCase().includes(this.searchInput.toLowerCase())
      )
    }
  }
}
</script>

<template>
  <div class="search-wrapper">
    <div id="to-content-ref"></div>
    <!-- sök -->
    <input v-model="searchInput" placeholder="Search tags or click below" class="search-bar" />

    <h3>Tags:</h3>
    <!-- sök med tags -->
    <TagItem v-for="tag in tags" :key="tag" :tag="tag" @tag-clicked="addTagToSearch" />
  </div>
  <!-- rendera projekt genom filter -->
  <article v-for="project in filteredProjects" :key="project.tags" class="project">
    <div class="content-img">
      <img :src="project.image" alt="Project Image" />
    </div>
    <div class="content-txt">
      <h2>{{ project.name }}</h2>
      <p>{{ project.description }}</p>
      <div class="tag-box">
        <h6>Tags:</h6>
        <h6 class="tags">{{ project.tags }}</h6>
      </div>
    </div>
  </article>
</template>

<style>
#to-content-ref {
  height: 2vh;
}

/* search */
.search-wrapper {
  padding: 3vh 0 4vh 0;
  text-align: center;
  background-color: #121212;
  border-bottom: 0.2vh solid #1c1c1c;
}
.search-wrapper h3 {
  margin: 2vh;
  color: #eeeeee;
}
.search-wrapper h6 {
  color: #ff4b2c;
  display: inline;
  margin: 1.5vh;
  cursor: pointer;
}
.search-bar {
  border: 0;
  border-radius: 0.5vw;
  padding: 1.5vh;
  width: 20vw;
}

/* content */
.project {
  display: flex;
  flex-direction: row;
  justify-content: center;
  background-color: #121212;
}

/* image */
.content-img {
  width: 60vw;
  margin-top: 4vh;
  margin-bottom: 4vh;
  margin-right: 0.1vw;
  text-align: center;
  background-color: #f1f1f1;
}
.project img {
  max-width: 58vw;
  max-height: 58vh;
  margin: 1vw;
}

/* text */
.content-txt {
  width: 15vw;
  margin-top: 4vh;
  margin-bottom: 4vh;
  margin-left: 0.1vw;
  text-align: left;
  background-color: #222222;
  border-radius: 0vh 2vh 2vh 0vh;
  color: #ffffff;
  position: relative;
  display: flex;
  flex-direction: column;
}
.project h2 {
  margin: 3vh 1vw 1vh 1vw;
  padding-bottom: 1vh;
  border-bottom: 2px solid #1c1c1c;
}
.project p {
  margin: 1vw;
  min-height: 3.5vh;
}
.content-txt .tag-box {
  margin: 1vh 1vw 3vh 1vw;
  margin-top: auto;
  padding-top: 1vh;
  border-top: 2px solid #1c1c1c;
}
.content-txt .tags {
  color: #ff4b2c;
}
@media only screen and (max-width: 1000px) {
  #to-content-ref {
    height: 5vh;
  }

  /* search */
  .search-wrapper {
    padding: 3vh 0 4vh 0;
    text-align: center;
    background-color: #121212;
    border-bottom: 0.2vh solid #1c1c1c;
  }
  .search-wrapper h3 {
    margin: 2vh;
    color: #eeeeee;
  }
  .search-wrapper h6 {
    color: #ff4b2c;
    display: inline;
    font-size: 0.95em;
    margin: 1.5vh;
    cursor: pointer;
  }
  .search-bar {
    border: 0;
    border-radius: 0.5vw;
    padding: 1.5vh;
    width: 75vw;
  }

  /* content */
  .project {
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-color: #121212;
  }

  /* image */
  .content-img {
    width: 80vw;
    margin: 5vh 10vw 0.5vh 10vw;
    text-align: center;
    background-color: #f1f1f1;
  }
  .project img {
    max-width: 80vw;
    max-height: 80vh;
    padding: 0.5vh;
    margin: 0;
  }

  /* text */
  .content-txt {
    width: 80vw;
    margin: 0 10vw 5vh 10vw;
    text-align: left;
    background-color: #222222;
    border-radius: 0vh 0vh 2vh 2vh;
    color: #ffffff;
  }
  .project h2 {
    margin: 3vw;
    padding-bottom: 2vh;
    border-bottom: 2px solid #1c1c1c;
  }
  .project p {
    margin: 3vw;
    min-height: 3.5vh;
  }
  .content-txt .tag-box {
    margin: 3vw;
    padding-top: 2vh;
    border-top: 2px solid #1c1c1c;
  }
  .content-txt .tags {
    color: #ff4b2c;
  }
}
</style>
