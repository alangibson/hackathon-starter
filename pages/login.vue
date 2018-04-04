<template>
  <div>
    <h3 class="page-header">Sign in</h3>
    <form class="form-horizontal" method="POST" action="/login">

      <input type="hidden" name="_csrf" :value="csrf" />

      <div class="form-group">
        <label class="col-sm-3 control-label" for="email">Email</label>
        <div class="col-sm-7">
          <input class="form-control" type="email" name="email" id="email" placeholder="Email" autofocus="true" required="true"/>
        </div>
      </div>

      <div class="form-group">
        <label class="col-sm-3 control-label" for="password">Password</label>
        <div class="col-sm-7">
          <input class="form-control" type="password" name="password" id="password" placeholder="Password" required="true"/>
        </div>
      </div>

      <div class="form-group">
        <div class="col-sm-offset-3 col-sm-7">
          <button class="col-sm-3 btn btn-primary" type="submit">
            <i class="far fa-user fa-sm"> Login</i>
          </button>
          <a class="btn btn-link" href="/forgot">Forgot your password?</a>
        </div>
      </div>

      <div class="form-group">
        <div class="col-sm-offset-3 col-sm-7">
          <hr/>
        </div>
      </div>

      <div class="form-group">
        <div class="col-sm-offset-3 col-sm-7">
          <a class="btn btn-block btn-facebook btn-social" href="/auth/facebook">
            <i class="fab fa-facebook-f fa-sm"></i>Sign in with Facebook
          </a>
          <a class="btn btn-block btn-twitter btn-social" href="/auth/twitter">
            <i class="fab fa-twitter-f fa-sm"></i>Sign in with Twitter
          </a>
          <a class="btn btn-block btn-google btn-social" href="/auth/google">
            <i class="fab fa-google-plus-g fa-xs"></i>Sign in with Google
          </a>
          <a class="btn btn-block btn-github btn-social" href="/auth/github">
            <i class="fab fa-github fa-sm"></i>Sign in with GitHub
          </a>
          <a class="btn btn-block btn-linkedin btn-social" href="/auth/linkedin">
            <i class="fab fa-linkedin-in fa-sm"></i>Sign in with LinkedIn
          </a>
          <a class="btn btn-block btn-instagram btn-social" href="/auth/instagram">
            <i class="fab fa-instagram fa-sm"></i>Sign in with Instagram
          </a>
        </div>
      </div>

    </form>
  </div>
</template>

<script>
export default {
  asyncData (context) {
    return { csrf: context.res.locals._csrf }
  }
}
</script>
