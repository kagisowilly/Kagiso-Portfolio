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
    <SidebarLink class="sidebarlink" to="/dashboard" icon="fas fa-columns">
      Dashboard
    </SidebarLink>
    <SidebarLink class="sidebarlink" to="/analytics" icon="fas fa-chart-bar">
      Analytics
    </SidebarLink>
    <SidebarLink class="sidebarlink" to="/friends" icon="fas fa-users">
      Friends
    </SidebarLink>
    <SidebarLink class="sidebarlink" to="/image" icon="fas fa-image">
      Images
    </SidebarLink>

    <span
      class="collapse-icon"
      :class="{ 'rotate-180': collapsed }"
      @click="toggleSidebar"
    >
      <i class="fas fa-angle-double-left" />
    </span>
  </div>
</template>

<style>
:root {
  --sidebar-bg-color: #2c5d45;
  --sidebar-item-hover: #2c5d45;
  --sidebar-item-active: #2c5d45;
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
  margin-top: 40px;
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
}
.profile2 {
  height: 250px;
  width: 220px;
  border-radius: 20px;
  float: left;
  border: white !important;
}
.profile1 {
  height: auto;
  width: 65px;
  border-radius: 20px;
  float: left;
  border: white !important;
}
</style>
