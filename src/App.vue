<script>
import Sidebar from '@/components/sidebar/Sidebar'
import { sidebarWidth } from '@/components/sidebar/state'
export default {
  components: { Sidebar },
  setup() {
    return { sidebarWidth }
  }
}
</script>
<template>
  <Sidebar />



  <div :style="{ 'margin-left': sidebarWidth }">
    <router-view />
      <!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header p-0">
        <h5 class="modal-title m-auto" id="exampleModalLabel">Profile Picture</h5>
      </div>
      <div class="modal-body  m-0 p-0">
      <img class="sideBarImage" src="@/assets/profile-min.jpg" alt="Nav-bar-image">
      </div>
    </div>
  </div>
</div>
  </div>

</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: rgb(242 242 252);
  color: #2c3e50;
  
}
p, .span, td{
  font-size: .9em;
  font-weight: bolder;
  color: #474747;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
section{
    overflow-x: hidden !important;
    overflow-y: hidden !important;
}
.subtitlee {
  color: #12613b;
}
/* MODAL */
.sideBarImage{
  width: 100%;
  border-bottom-right-radius:20px ;
  border-bottom-left-radius:20px ;
}
.modal-content{
  width: auto;
  border-radius: 20px;
}
@media all and(max-width:500px){
  .sideBarImage{
  width: 80%;
}
}
</style>
