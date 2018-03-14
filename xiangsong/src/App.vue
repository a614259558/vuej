<template>
  <div id="app">
    <CommonHead></CommonHead>
    <IndexBanner></IndexBanner>
    <Nav></Nav>
    <IndexFooter></IndexFooter>
  </div>
</template>

<script>
import CommonHead from './components/CommonHead'
import IndexBanner from './components/IndexBanner'
import Nav from './components/Nav'
import IndexFooter from './components/IndexFooter'

export default {
  name: 'App',
  components : {
    CommonHead,
    IndexBanner,
    Nav,
    IndexFooter
  }
}
</script>

<style>
  
</style>
