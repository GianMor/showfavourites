<template>
  <div class="list">
    <div class="title">
      <h1>Teams</h1>
    </div>
    <div class="show-preferiti">
      <input v-model="show" type="checkbox" name="btn" id="btn">
      <label for="btn" class="myButton">Mostra preferiti</label>
    </div>
    <div>
      <div v-if="show">
        <div class="pers-list">
          <div v-for="item in item1" v-bind:key="item.id" class="img-pers">
            <div class="img">
              <img :src="item.img">
            </div>
            <div class="pers-info">
              <h3>{{ item.name }} {{ item.surname }}</h3>
              <h5>{{ item.nickname }}</h5>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "List",
  props: {
    msg: String
  },
  data: function() {
    return {
      show: true,
      item1: [
        {
          id: 1,
          img: 'https://pbs.twimg.com/profile_images/722410465091956736/ob1w9NIE_400x400.jpg',
          name: "Steve",
          surname: "Roger",
          nickname: "Captain America"
        },
        {
          id: 2,
          img: "https://nerdmovieproductions.it/wp-content/uploads/2017/07/robert-downey-jr-ironman.jpg",
          name: "Tony",
          surname: "Stark",
          nickname: "Iron man"
        },
        {
          id: 3,
          img: "http://www.ciakclub.it/wp-content/uploads/2018/06/avengers_black_widow-black-widow-is-confirmed-for-battle-in-civil-war-jpeg-224673-970x545.jpg",
          name: "Natasha",
          surname: "Romanoff",
          nickname: "Black widow"
        },
        {
          id: 4,
          img: "https://uproxx.files.wordpress.com/2019/02/captain-marvel.jpg?quality=100&w=650 ",
          name: "Carol",
          surname: "Danvers",
          nickname: "Captain Marvel"
        },
        {
          id: 5,
          img: "https://www.dhresource.com/0x0s/f2-albu-g10-M01-73-6D-rBVaVlxkvB-AVOGTAAJ8-He6lfo368.jpg/tree-man-flower-pot-portapenne-change-jar.jpg",
          name: "Grut",
          surname: "Grut",
          nickname: "Grut"
        },
        {
          id: 6,
          img: "https://cdn.images.express.co.uk/img/dynamic/36/590x/SCARLETT-WITCH-826346.jpg",
          name: "Wanda",
          surname: "Maximoff",
          nickname: "Scarlet Witch"
        }
      ]
    };
  }
};
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

img {
  width: 5rem;
  height: 5rem;
  float: left;
  border-radius: 50% 50%;
}

.list {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
}

.title {
  text-align: center;
}

.show-preferiti {
  text-align: center;
}
.pers-list {
  width: 50%;
  height: 5rem;
  margin: 2.5rem auto;
}

.img {
  width: 50%;
  height: 10%;
  margin: 0 auto;
}

.pers-info {
  height: 5rem;
  width: 25%;
  margin: 0 auto;
  text-align: center;
}
input {
  display: none;
}
label {
  cursor: pointer;
  padding: 0.5rem .5rem;
  background-color: aqua;
}
.myButton {
	-moz-box-shadow: -4px 4px 0px 0px #3dc21b;
	-webkit-box-shadow: -4px 4px 0px 0px #3dc21b;
	box-shadow: -4px 4px 0px 0px #3dc21b;
	background-color:transparent;
	-moz-border-radius:42px;
	-webkit-border-radius:42px;
	border-radius:42px;
	border:2px solid #18ab29;
	display:inline-block;
	cursor:pointer;
	color:black;
	font-family:Georgia;
	font-size:22px;
	padding:15px 76px;
	text-decoration:none;
	text-shadow:-2px 4px 1px #2f6627;
}
.myButton:hover {
	background-color:transparent;
}
.myButton:active {
	position:relative;
	top:1px;
}

</style>
