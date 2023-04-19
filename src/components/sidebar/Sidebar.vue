<script>
import SidebarLink from './SidebarLink'
import { collapsed, toggleSidebar, sidebarWidth } from './state'

export default {
  props: {},
  components: { SidebarLink },
  setup() {
    return { collapsed, toggleSidebar, sidebarWidth }
  }
  
}
</script>

<template>
  <div class="sidebar " :style="{ width: sidebarWidth }">
    <div class="nav-image" data-bs-toggle="modal" data-bs-target="#exampleModal">
        <div class="col col-lg-10 abountcont col-md-10">
          <img
            src="@/assets/profile-min.jpg"
            alt="profile"
            class="img-responsive profile1"
          />
        </div>
    </div>
            <!-- Button trigger modal -->



    <SidebarLink title="Home" class="sidebarlink" to="/" icon="fas fa-home">
      Home
    </SidebarLink>
    <SidebarLink title="About" class="sidebarlink" to="/about" icon="fas fa-address-card">
      About
    </SidebarLink>
    <SidebarLink title="Resume" class="sidebarlink" to="/resume" icon="fas fa-list">
      Resume
    </SidebarLink>
    <SidebarLink title="Skills" class="sidebarlink" to="/skills" icon="fas fa-pen">
      Skills
    </SidebarLink>
    <SidebarLink title="Projects" class="sidebarlink" to="/projects" icon="fas fa-suitcase">
      Projects
    </SidebarLink>
        <SidebarLink title="Testimonials" class="sidebarlink" to="/testimonials" icon="fas fa-users">
      Testimonials
    </SidebarLink>
        <SidebarLink title="Contact" class="sidebarlink" to="/contact" icon="fas fa-comments">
      Contact
    </SidebarLink>

        <div class="footer-copyright copy1 text-center mb-0 py-1 text-white">
          ©2022:KM
        </div>      
  </div>
</template>

<style>
.sidebarlink.active {
  color: rgba(115, 179, 106, 0.966);
  font-weight: 600;
}
.copy1{
position: absolute !important;
bottom:50px !important;
}
.copy2{
position: absolute !important;
bottom:50px !important;
}
.footer-copyright{
  position: absolute;
  bottom: 10;
  font-size: 10px;
}
:root {
  --sidebar-bg-color: #1d4632;
  --sidebar-item-hover: #1d4632;
  --sidebar-item-active: #1d4632;
}
</style>

<style scoped>
.sidebar {
  color: white;
  background-color: var(--sidebar-bg-color);

  float: left;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  bottom: 0;
  padding: 0.5em;

  transition: 0.3s ease;

  display: flex;
  flex-direction: column;
}


.sidebar h1 {
  height: 2.5em;
}

.sidebarlink {
  margin-top: 25px;
    font-size: .9em !important;
  font-weight: bolder !important;
}
.collapse-icon {
  position: absolute;
  bottom: 0;
  padding: 0.75em;

  color: rgba(255, 255, 255, 0.7);

  transition: 0.2s linear;
}

.rotate-180 {
  transform: rotate(180deg);
  transition: 0.2s linear;
}
.collapse-icon {
  font-size: 30px;
      padding: 0px;
}
.profile2 {
  height: 210px;
  width: 190px;
  border-radius: 20px;
  float: left;
  border: white !important;
  object-fit: cover;
}
.profile1 {
  height: auto;
  width: 65px;
  border-radius: 20px;
  float: left;
  border: white !important;
}
.nav-image{
  cursor: pointer;
}
.sidebarlink:hover{
  -ms-transform: scale(1.2);
  -webkit-transform: scale(1.2);
  transform: scale(1.2); 
  color:rgba(115, 179, 106, 0.966) !important;
  width: 70%;
}
.fa-angle-double-left:hover{
  -ms-transform: scale(1.2);
  -webkit-transform: scale(1.2);
  transform: scale(1.2); 
  color:rgba(115, 179, 106, 0.966) !important;
  width: 70%;
}
@media all and (max-width:768px) {
  .collapse-icon{
    display: none;
  }
  .footer-copyright{
    position: fixed !important;
    bottom: 5;
  }
}
</style>
