<template>
  <div class="navbar">
    <div class="icon">
      <h2 class="logo">W.Tech.</h2>
    </div>
    <div class="menu">
      <ul>
        <li><router-link to="/">HOME</router-link></li>
        <li><router-link to="/about">ABOUT</router-link></li>
        <li><router-link to="/profile">PROFILE</router-link></li>
        <li><router-link to="/photos">PHOTOS</router-link></li>
        <li><a href="#">CONTACT US</a></li>
      </ul>
    </div>
    <div class="search">
      <input class="srch" type="search" v-model="searchTerm" @input="searchPhotos" placeholder="Search photos...">
    </div>
  </div>
</template>

<script>
import { mapActions } from 'vuex';

export default {
  data() {
    return {
      searchTerm: '',
    };
  },
  methods: {
    ...mapActions(['filterPhotos']),
    searchPhotos() {
      this.filterPhotos(this.searchTerm);
    },
  },
};
</script>

<style scoped>
.navbar {
  width: 100%;
  height: 75px;
  margin: auto;
}

.icon {
  width: 20%;
  float: left;
  height: 70px;
}

.logo {
  color: #fc8d1e;
  font-size: 20px;
  font-family: Cambria;
  padding-left: 50px;
  float: left;
  padding-top: 10px;
  margin-top: 5px;
}

.menu {
  width: 50%;
  float: left;
  height: 70px;
}

ul {
  float: left;
  display: flex;
  justify-content: center;
  align-items: center;
}

li {
  list-style: none;
  margin-left: 30px;
  margin-top: 27px;
  font-size: 14px;
}

ul li a {
  text-decoration: none;
  color: #fff;
  font-family: Arial;
  font-weight: bold;
  transition: 0.4s ease-in-out;
}

ul li a:hover {
  color: #ff7200;
}

.search {
  width: 29%;
  float: left;
  margin-left: 1%;
}

.srch {
  font-family: 'Times New Roman';
  width: 150px;
  height: 30px;
  background: transparent;
  border: 1px solid #ff7200;
  margin-top: 20px;
  color: #fff;
  border-right: none;
  font-size: 16px;
  float: left;
  padding: 10px;
  border-bottom-left-radius: 5px;
  border-top-left-radius: 5px;
}

.srch:focus {
  outline: none;
}

</style>


