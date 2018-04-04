<template>
  <div>
    <h3 class="page-header">Sign up</h3>

    <form id="signup-form" class="form-horizontal" method="POST" action="/signup">

      <input type="hidden" name="_csrf" :value="csrf" />

      <div class="form-group">
        <label class='col-sm-3 control-label' for='email'>Email</label>
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
        <label class="col-sm-3 control-label" for="confirmPassword">Confirm Password</label>
        <div class="col-sm-7">
          <input class="form-control" type="password" name="confirmPassword" id="confirmPassword"
                 placeholder="Confirm Password" required="true"/>
        </div>
      </div>

      <div class="form-group">
        <div class="col-sm-offset-3 col-sm-7">
          <button class="btn btn-success" type="submit">
            <i class="fas fa-user-plus fa-sm"></i>
            Signup
          </button>
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
