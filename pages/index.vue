<template>
  <div>
    <Project />
    <Activity />
    <Profile />
  </div>
</template>
<script>
import Project from '@/components/project'
import Activity from '@/components/activity'
import Profile from '@/components/profile'
export default {
  components: {
    Project,
    Activity,
    Profile,
  },
}
</script>
<style scoped>
.project {
  background: -webkit-linear-gradient(to right, #36aa37 0%, #2da8aa 50%)
    no-repeat !important;
  background: linear-gradient(to right, #36aa37 0%, #2da8aa 50%) no-repeat !important;
}
.activity {
  background-color: #000000;
}
.profile {
  background: -webkit-linear-gradient(to right, #36aa37 0%, #2da8aa 50%)
    no-repeat !important;
  background: linear-gradient(to right, #36aa37 0%, #2da8aa 50%) no-repeat !important;
}
</style>
