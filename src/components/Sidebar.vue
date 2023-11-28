<script>
import SidebarLink from './SidebarLink.vue'
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
  <div class="sidebar" :style="{ width: sidebarWidth }">
    <h1>
      <span v-if="collapsed">
        <div>ET</div>
        <div>CRM</div>
      </span>
      <span v-else>Evitalyst CRM</span>
    </h1>
<br>

<SidebarLink to="/homeview" icon="fas fa-house">Dashboard</SidebarLink>
<SidebarLink to="/analytics" icon="fas fa-address-card">Leads</SidebarLink>
<SidebarLink to="/image" icon="fas fa-money-check">Deals</SidebarLink>
<SidebarLink to="/friends" icon="far fa-id-card">Contacts</SidebarLink>
<SidebarLink to="/image" icon="fas fa-user-tie">Customer</SidebarLink>
<SidebarLink to="/image" icon="fas fa-rectangle-list">Report</SidebarLink>
<SidebarLink to="/image" icon="fas fa-business-time">Sales Stage</SidebarLink>

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
  --sidebar-bg-color: rgb(51, 95, 226);
  --sidebar-item-hover: rgb(93, 56, 161);
  --sidebar-item-active: #343aeb
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
</style>