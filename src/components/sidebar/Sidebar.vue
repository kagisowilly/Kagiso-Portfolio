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
    <div>
      <span  v-if="collapsed">
        <div class="col col-lg-10 abountcont col-md-10">
          <img
            src="@/assets/profile-min.jpg"
            alt="profile"
            class="img-responsive profile1"
          />
        </div>
      </span>
      <span v-else>
        <div class="col col-lg-10 abountcont col-md-10">
          <img
            src="@/assets/profile-min.jpg"
            alt="profile"
            class="img-responsive  profile2"
          />
        </div>
      </span>
    </div>

    <SidebarLink class="sidebarlink" to="/" icon="fas fa-home">
      Home
    </SidebarLink>
    <SidebarLink class="sidebarlink" to="/about" icon="fas fa-address-card">
      About
    </SidebarLink>
    <SidebarLink class="sidebarlink" to="/resume" icon="fas fa-list">
      Resume
    </SidebarLink>
    <SidebarLink class="sidebarlink" to="/skills" icon="fas fa-pen">
      Skills
    </SidebarLink>
    <SidebarLink class="sidebarlink" to="/projects" icon="fas fa-suitcase">
      Projects
    </SidebarLink>
        <SidebarLink class="sidebarlink" to="/testimonials" icon="fas fa-users">
      Testimonials
    </SidebarLink>
        <SidebarLink class="sidebarlink" to="/contact" icon="fas fa-comments">
      Contact
    </SidebarLink>

    <span
      class="collapse-icon "
      :class="{ 'rotate-180': collapsed }"
      @click="toggleSidebar"
    >
      <i class="fas  fa-angle-double-left" />
    </span>
    <span v-if="collapsed">
        <div class="footer-copyright copy1 text-center mb-0 py-1 text-white">
          ©2022:KM
        </div>      
    </span>
    <span v-else>
        <div class="footer-copyright copy2 text-center mb-0 py-1 text-white">
          ©2022 Copyright: Kagiso Mphayi
        </div>         
    </span>

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
  height: 250px;
  width: 220px;
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
</style>
