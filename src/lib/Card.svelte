<script>
export let title;
export let text;
export let pictureURL;
</script>

<main>
<div class="card" style="background-image: url({pictureURL})">
  <div class="pt1">
    <img id="icon-img" src={pictureURL} alt="user">
  </div>
  <div class="pt2">
    <h3 id="p2header">{title}</h3>
    <p id="p2text">{text}</p>
  </div>

</div>
</main>

<style>
  * {
    padding: 0;
    margin: 0;
  }
.card {
  display: flex;
  flex-direction: column;
  background-repeat: no-repeat;
  background-color: rgba(255,255,255, 0.6);
  background-blend-mode: lighten;
  width: 190px;
  height: 270px;
  border: 4px solid grey;
  border-radius: 15px;
  padding: 15px;
}

.card:hover {
  cursor: pointer;
}

.pt1 {
  width: 100%;
  height: 100%;
  border-radius: 15px;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

.pt2 {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.pt2 h3 {
  text-align: center;
}

#p2header {
  margin: 5px 0;
  padding-bottom: 5px;
  border-bottom: 3px solid grey;
}

#p2text {
  padding: 5px;
  background-color: rgba(255,255,255, 0.8);
  background-blend-mode: lighten;
  border-radius: 10px;
}

#icon-img {
  width: 90px;
  height: 90px;
  border-radius: 100%;
}
</style>
