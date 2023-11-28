<template>
  <div class="wrapper">
    <!-- Sidebar -->
    <div class="sidebar" :data-image="require('@/assets/img/sidebar-5.jpg')">
      <div class="sidebar-wrapper">
        <div class="logo">
          <a href="javascript:;" class="simple-text">
            Your Logo
          </a>
        </div>
        <ul class="nav">
          <li class="nav-item active">
            <router-link to="/dashboard" class="nav-link">
              <i class="nc-icon nc-paper-2"></i>
              <p>First example</p>
            </router-link>
          </li>
          <li class="nav-item">
            <router-link to="/user" class="nav-link">
              <i class="nc-icon nc-bell-55"></i>
              <p>Second example</p>
            </router-link>
          </li>
          <li class="nav-item active active-pro">
            <router-link to="/upgrade" class="nav-link">
              <i class="nc-icon nc-alien-33"></i>
              <p>Upgrade plan</p>
            </router-link>
          </li>
        </ul>
      </div>
    </div>
    <!-- End Sidebar -->

    <!-- Main Panel -->
    <div class="main-panel">
      <!-- Navbar -->
      <nav class="navbar navbar-expand-lg" color-on-scroll="500">
        <div class="container-fluid">
          <router-link to="/" class="navbar-brand">Template</router-link>
          <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navigation" aria-controls="navigation-index" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-bar burger-lines"></span>
            <span class="navbar-toggler-bar burger-lines"></span>
            <span class="navbar-toggler-bar burger-lines"></span>
          </button>
          <div class="collapse navbar-collapse justify-content-end" id="navigation">
            <ul class="nav navbar-nav mr-auto">
              <li class="nav-item">
                <a href="#" class="nav-link" data-toggle="dropdown">
                  <i class="nc-icon nc-palette"></i>
                  <span class="d-lg-none">Dashboard</span>
                </a>
              </li>
              <li class="dropdown nav-item">
                <a href="#" class="dropdown-toggle nav-link" data-toggle="dropdown">
                  <i class="nc-icon nc-planet"></i>
                  <span class="notification">5</span>
                  <span class="d-lg-none">Notification</span>
                </a>
                <ul class="dropdown-menu">
                  <a class="dropdown-item" href="#">Notification 1</a>
                  <a class="dropdown-item" href="#">Notification 2</a>
                  <a class="dropdown-item" href="#">Notification 3</a>
                  <a class="dropdown-item" href="#">Notification 4</a>
                  <a class="dropdown-item" href="#">Another notification</a>
                </ul>
              </li>
              <li class="nav-item">
                <a href="#" class="nav-link">
                  <i class="nc-icon nc-zoom-split"></i>
                  <span class="d-lg-block">&nbsp;Search</span>
                </a>
              </li>
            </ul>
            <ul class="navbar-nav ml-auto">
              <li class="nav-item">
                <a class="nav-link" href="#pablo">
                  <span class="no-icon">Account</span>
                </a>
              </li>
              <li class="nav-item dropdown">
                <a class="nav-link dropdown-toggle" href="http://example.com" id="navbarDropdownMenuLink" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                  <span class="no-icon">Dropdown</span>
                </a>
                <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                  <a class="dropdown-item" href="#">Action</a>
                  <a class="dropdown-item" href="#">Another action</a>
                  <a class="dropdown-item" href="#">Something</a>
                  <a class="dropdown-item" href="#">Something else here</a>
                  <div class="divider"></div>
                  <a class="dropdown-item" href="#">Separated link</a>
                </div>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#pablo">
                  <span class="no-icon">Log out</span>
                </a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
      <!-- End Navbar -->
      
      <!-- Your router-view or page content goes here -->
      <router-view></router-view>
    </div>
    <!-- End Main Panel -->
  </div>
</template>

<script>
export default {
  // Add your component-specific logic here
}
</script>

<style scoped>
/* Add component-specific styles here */

/* Sidebar Styles */
.sidebar {
  width: 260px;
  position: fixed;
  background: #333;
  color: #fff;
  height: 100%;
  overflow-y: auto;
  overflow-x: hidden;
  top: 0;
  left: 0;
  z-index: 1;
  transition: all 0.3s;
}

.sidebar-wrapper {
  padding-top: 20px;
}

.logo {
  text-align: center;
}

.logo a {
  display: block;
  color: #fff;
  text-decoration: none;
  font-size: 20px;
}

.nav {
  list-style-type: none;
  padding: 0;
}

.nav-item {
  margin-bottom: 10px;
}

.nav-link {
  color: #fff;
  text-decoration: none;
  display: block;
  padding: 10px;
  border-radius: 4px;
  transition: background 0.3s;
}

.nav-link:hover {
  background: rgba(255, 255, 255, 0.1);
}

/* Main Panel Styles */
.main-panel {
  margin-left: 260px;
  transition: margin-left 0.3s;
}

/* Navbar Styles */
.navbar {
  background: #fff;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  padding: 15px;
}

.navbar-brand {
  font-size: 1.5em;
  color: #333;
  text-decoration: none;
}

.navbar-toggler {
  border: none;
}

.navbar-toggler-bar {
  background: #333;
  height: 3px;
  margin: 6px 0;
  width: 25px;
}

/* Page Content Styles */
.wrapper {
  min-height: 100vh;
  position: relative;
}

/* Customize other styles based on your needs */

</style>
