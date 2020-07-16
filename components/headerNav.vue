<template>
  <div>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/">Top</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/detailProject">Project</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/detailActivity">Activity</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/detailProfile">Profile</nuxt-link>
        </li>
      </ul>
    </nav>
  </div>
</template>
<style lang="scss" scoped>
nav {
  color: #fff;
  ul {
    display: flex;
    justify-content: flex-end;
    li {
      list-style-type: none;
      margin-left: 15px;
      a {
        color: #fff;
      }
    }
  }
}
</style>
