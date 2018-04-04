<template>
  <div>

    <!-- TODO Needs to be child of BODY tag -->
    <div class="navbar navbar-default navbar-fixed-top">
      <div class="container">
        <div class="navbar-header">

          <button class="navbar-toggle" type='button' data-toggle='collapse' data-target='.navbar-collapse'>
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>

          <a class="navbar-grand" href="/">
            <i class="fas fa-cube"></i>
            Project name
          </a>

        </div>
      </div>
    </div>

    <nuxt/>

  </div>
</template>

<script>
export default {
  // Called by Nuxt's vue-meta plugin
  head () {
    return {
      title: 'nuxt-starter',
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        { hid: 'description', name: 'description', content: 'Nuxt.js project' }
      ],
      link: [
        { rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' },
        // Reusing the Hackathon Starter css
        { rel: 'stylesheet', href: '/css/main.css' }
      ],
      script: [
        { src: '/js/lib/jquery-3.1.1.min.js', type: 'text/javascript' },
        { src: '/js/lib/bootstrap.min.js', type: 'text/javascript' },
        { src: '/js/main.js', type: 'text/javascript' }
      ]
    }
  }
}
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
