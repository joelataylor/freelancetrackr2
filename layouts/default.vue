<template>
  <div class="flex h-screen">
    <nav class="flex flex-col items-center w-16 lg:w-48 pt-4 lg:pt-0 bg-blue text-blue-light text-left">
      <Avatar />

      <div class="flex flex-col w-full mt-4">

        <NavItem href="/projects" icon="fa-server">Projects</NavItem>
        <NavItem href="/invoices" icon="fa-leaf">Invoices</NavItem>
        <NavItem href="/clients" icon="fa-graduation-cap">Clients</NavItem>
        <NavItem href="/reports" icon="fa-chart-bar">Reports</NavItem>
        <NavItem href="/settings" icon="fa-cogs">Settings</NavItem>

        <Logo />

      </div>
    </nav>

    <nuxt/>
  </div>
</template>

<script>
import Avatar from '@/components/Avatar'
import NavItem from '@/components/NavItem'
import Logo from '@/components/Logo'

export default {
  components: {
    Avatar,
    Logo,
    NavItem
  }
}
</script>


<style>
html
{
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*, *:before, *:after
{
  box-sizing: border-box;
  margin: 0;
}
.button--green
{
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}
.button--green:hover
{
  color: #fff;
  background-color: #3b8070;
}
.button--grey
{
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}
.button--grey:hover
{
  color: #fff;
  background-color: #35495e;
}
</style>
