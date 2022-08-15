<script>
    import Card from './Card.svelte'
    const cardStuff = [
        {
            title: "All Users",
            text: "Search for and manage users information.",
            pictureURL: "src/assets/user.png"
        },
        {
            title: "Import Users",
            text: "Add users to the platform.",
            pictureURL:"src/assets/import.png"
        },
        {
            title: "Meeting Organizers",
            text: "Set who can schedule connections and organize meetings.",
            pictureURL:"src/assets/videoconference.png"
        },
        {
            title: "Meeting Categories",
            text: "Categorize your meeting organizers into subject types.",
            pictureURL:"src/assets/teacher.png"
        },
        {
            title: "Branding",
            text: "Customize the site colors and logos to match your school or organization.",
            pictureURL:"src/assets/web-design.png"
        },
        {
            title: "Card Management",
            text: "Customize cards to provide users with easy access to important apps and websites.",
            pictureURL:"src/assets/cards.png"
        },
        {
            title: "Tags",
            text: "Create tags to organize your users.",
            pictureURL:"src/assets/tag.png"
        },
    ]
</script>

<main>
    <h1>Site Management</h1>
    <ul>
        <li>
            <input type="checkbox" checked>
            <i></i>
            <h2>User Management</h2>
            <div class="expand">
                <Card {...cardStuff[0]} />
                <Card {...cardStuff[1]} />
                <Card {...cardStuff[6]} />
            </div>
        </li>
      <li>
        <input type="checkbox" checked>
        <i></i>
        <h2>Meeting Settings</h2>
        <div class="expand">
            <Card {...cardStuff[2]} />
            <Card {...cardStuff[3]} />
        </div>
      </li>
      <li>
        <input type="checkbox" checked>
        <i></i>
        <h2>Site Settings</h2>
        <div class="expand">
            <Card {...cardStuff[4]} />
            <Card {...cardStuff[5]} />
        </div>
      </li>
    </ul>
</main>

<style>
div {
  transition: transform 0.25s ease-in;
}

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
  font-weight: 100;
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
  border-top: 2px solid #dce7eb;
}
ul li i {
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
}
ul li input[type=checkbox] {
  position: absolute;
  cursor: pointer;
  width: 100%;
  height: 100%;
  z-index: 1;
  opacity: 0;
}
ul li input[type=checkbox]:checked ~ div{
  margin-top: 0;
  max-height: 0;
  opacity: 0;
  transform: translate(0, 30%);
}
ul li input[type=checkbox]:checked ~ i:before {
  transform: translate(2px, 0) rotate(45deg);
}
ul li input[type=checkbox]:checked ~ i:after {
  transform: translate(-2px, 0) rotate(-45deg);
}

.expand {
    display: flex;
    flex-direction: row;
    padding: 15px 0;
    gap: 15px;
}
</style>