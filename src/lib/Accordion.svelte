<script>
    import Card from './Card.svelte'
    const categories = ["community","content","education","connections","questionnaire","users"]

    const communityStuff = [
      {
        id: 1,
        title: "Announcements",
        text: "Create announcements displayed at the top of the Home feed.",
        pictureURL:"src/assets/megaphone.png"
      },
      {
        id: 2,
        title: "Events",
        text: "Configure public events that users can sign up for.",
        pictureURL:"src/assets/conference.png"
      }
    ]

    const contentStuff =  [
      {
        id: 1,
        title: "Branding",
        text: "Customize the site colors and logos to match your school or organization.",
        pictureURL:"src/assets/web-design.png"
      },
      {
        id: 2,
         title: "Card Management",
         text: "Customize cards to provide users with easy access to important apps and websites.",
         pictureURL:"src/assets/cards.png"
      },
      {
        id: 3,
         title: "RSS Feeds",
         text: "Set up RSS feed sources that are dispalyed to users.",
         pictureURL:"src/assets/rss.png"
      },
      {
        id: 4,
         title: "Twitter feed sources",
         text: "Configure the Twitter Feed Sources displayed on the Home feed.",
         pictureURL:"src/assets/twitter.png"
      },
      {
        id: 5,
         title: "Document types",
         text: "Define the document types in the platform.",
         pictureURL:"src/assets/documents.png"
      },

    ]

    const educationStuff = [
      {
        id: 1,
         title: "Courses",
         text: "Assign courses from your LMS that are available for users to enroll in.",
         pictureURL:"src/assets/online-course.png"
      }
    ]

    const connectionsStuff = [
      {
        id: 1,
         title: "Meeting Organizers",
         text: "Set who can schedule connections and organize meetings.",
         pictureURL:"src/assets/videoconference.png"
      },
      {
        id: 2,
         title: "Meeting Categories",
         text: "Categorize your meeting organizers into subject types.",
         pictureURL:"src/assets/teacher.png"
      }
    ]

    const questionnaireStuff = [
      {
        id: 1,
         title: "Questions",
         text: "Customize the questions shown to users in the questionnaire.",
         pictureURL:"src/assets/question.png"
      },
      {
        id: 2,
         title: "Suggested Answers",
         text: "Configure the answers that users can provide in the questionnaire. ",
         pictureURL:"src/assets/answer.png"
      }
    ]

    const usersStuff = [
        {
          id: 1,
           title: "All Users",
           text: "Search for and manage users information.",
           pictureURL: "src/assets/user.png"
        },
        {
          id: 2,
           title: "Import Users",
           text: "Add users to the platform.",
           pictureURL:"src/assets/import.png"
        },
        {
          id: 3,
           title: "Tags",
           text: "Create tags to organize your users.",
           pictureURL:"src/assets/tag.png"
        },
    ]

</script>

<main style="background-color: white; padding: 25px;">
    <h1>Site Administration</h1>
    <ul>
      <li>
          <!-- <input type="checkbox" checked> -->
          <!-- <i></i> -->
          <h2>{categories[0].toUpperCase()}</h2>
          <div class="expand">
            {#each communityStuff as current}
            <Card {...current} />
            {/each}
          </div>
      </li>
      <li>
        <!-- <input type="checkbox" checked> -->
        <!-- <i></i> -->
        <h2>{categories[1].toUpperCase()}</h2>
        <div class="expand">
          {#each contentStuff as current}
          <Card {...current} />
          {/each}
        </div>
      </li>
      <li>
        <!-- <input type="checkbox" checked> -->
        <!-- <i></i> -->
        <h2>{categories[2].toUpperCase()}</h2>
        <div class="expand">
          {#each educationStuff as current}
          <Card {...current} />
          {/each}
        </div>
      </li>
      <li>
        <!-- <input type="checkbox" checked> -->
        <!-- <i></i> -->
        <h2>{categories[3].toUpperCase()}</h2>
        <div class="expand">
          {#each connectionsStuff as current}
          <Card {...current} />
          {/each}
        </div>
      </li>
      <li>
        <!-- <input type="checkbox" checked> -->
        <!-- <i></i> -->
        <h2>{categories[4].toUpperCase()}</h2>
        <div class="expand">
          {#each questionnaireStuff as current}
          <Card {...current} />
          {/each}
        </div>
      </li>
      <li>
        <!-- <input type="checkbox" checked> -->
        <!-- <i></i> -->
        <h2>{categories[5].toUpperCase()}</h2>
        <div class="expand">
          {#each usersStuff as current}
          <Card {...current} />
          {/each}
        </div>
      </li>
    </ul>
</main>

<style>
/* div {
  transition: transform 0.25s ease-in;
} */

h2 {
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

h1 {
  text-transform: uppercase;
  font-size: 36px;
  line-height: 42px;
  letter-spacing: 3px;
}

h2 {
  font-size: 26px;
  line-height: 34px;
  font-weight: 300;
  letter-spacing: 1px;
  display: block;
  background-color: #fefffa;
  margin: 0;
  cursor: pointer;
}

ul {
  list-style: none;
  perspective: 900;
  padding: 0;
  margin: 0;
}
ul li {
  position: relative;
  padding: 0;
  margin: 0;
  padding-bottom: 4px;
  padding-top: 18px;
  border-top: 3px solid #dce7eb;
}
/* ul li i {
  position: absolute;
  transform: translate(-6px, 0);
  margin-top: 16px;
  right: 0;
}
ul li i:before, ul li i:after {
  content: "";
  position: absolute;
  background-color: gray;
  width: 3px;
  height: 9px;
}
ul li i:before {
  transform: translate(-2px, 0) rotate(45deg);
}
ul li i:after {
  transform: translate(2px, 0) rotate(-45deg);
} */
/* ul li input[type=checkbox] {
  position: absolute;
  cursor: pointer;
  width: 100%;
  height: 100%;
  opacity: 0;
} */
/* ul li input[type=checkbox]:checked ~ div{
  margin-top: 0;
  max-height: 0;
  opacity: 0;
  transform: translate(0, 30%);
} */
/* ul li input[type=checkbox]:checked ~ i:before {
  transform: translate(2px, 0) rotate(45deg);
}
ul li input[type=checkbox]:checked ~ i:after {
  transform: translate(-2px, 0) rotate(-45deg);
} */

.expand {
    display: flex;
    flex-direction: row;
    padding: 15px 0;
    gap: 15px;
}
</style>