<template>
  <div class="sidebar">
    <div class="text-center">
      <img src="@/assets/profile.jpg" alt="Profile Image">
      <h5>Jaehyun</h5>
    </div>
    
    <div>
      <ul>
        <li>   
          <router-link :to="{name: 'Dashboard'}"><font-awesome-icon icon="house-chimney" />Dashboard</router-link>
        </li>
        <slot></slot>
        <li>         
          <router-link :to="{name: 'UpdateProfile'}"><font-awesome-icon icon="user" />Update Profile</router-link>
        </li>
        </ul>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.sidebar {
    padding-top: 100px;
    min-width: 350px;
    height: 100%;
    background-color: #3d3657;
}

.sidebar img {
    width: 150px;
    height: 150px;
    border-radius: 100px;
    margin-bottom: 10px;
}

.sidebar h5 {
    color: white;
    margin-bottom: 50px;
}

.sidebar ul {
    list-style-type: none;
    padding-left: 0px !important;
}

.sidebar a {
    text-decoration: none;
    display: block;
    color: white;
    font-size: 1.2em;
    width: 100%;
    padding-left: 70px;
    line-height: 60px;
    box-sizing: border-box;
    transition: 0.3s;
    transition-property: background;
}

.sidebar svg {
    color: white;
    margin-right: 10px;
}

.sidebar a:hover {
    background-color: #595078;
    color: white;
}

.sidebar .active {
    background-color: #595078;
}
</style>