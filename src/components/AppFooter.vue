<script></script>

<template>
  <footer class="info">
    <p>Double-click to edit a todo</p>
    <p>
      An iteration on
      <a href="https://todomvc.com/examples/vue/">TodoMVC - Vue</a>
    </p>
    <p>
      Source Code:
      <a href="https://github.com/bencodezen/todomvc-vue-3">GitHub Repo</a>
    </p>
    <p class="netlify-sponsor">
      <span>Powered by</span
      ><a
        class="netlify-link"
        href="https://www.netlify.com/?utm_source=deployed-app&amp;utm_medium=launch-comp-bh&amp;utm_campaign=devex"
        ><img
          class="netlify-logo"
          src="/netliheart.svg"
          alt="Netlify Heart Logo"
        />
        Netlify
      </a>
    </p>
  </footer>
</template>

<style scoped>
.info {
  margin: 65px auto 0;
  color: #222;
  font-size: 1rem;
  text-shadow: 0 1px 0 rgba(255, 255, 255, 0.5);
  text-align: center;
}

.info p {
  line-height: 1;
}

.info a {
  color: inherit;
  text-decoration: none;
  font-weight: 400;
}

.info a:hover {
  text-decoration: underline;
}

.info .netlify-sponsor {
  justify-content: center;
}

.info .netlify-sponsor,
.info .netlify-link {
  display: flex;
  align-items: center;
}
.info .netlify-logo {
  width: 30px;
  margin-left: 5px;
  margin-right: 5px;
}
</style>
