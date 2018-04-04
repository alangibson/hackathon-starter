<template>
  <div>

    <div class="page-header">
      <h3>Contact Form</h3>
    </div>

    <form class="form-horizontal" method="POST" action="/contact">
      <input type="hidden" name="_csrf" :value="csrf" />

      <div class="form-group">
        <label class='col-sm-2 control-label' for="name">Name</label>
        <div class="col-sm-8">
          <input class="form-control" type='text' name='name' id='name' autofocus=true />
        </div>
      </div>

      <div class="form-group">
        <label class='col-sm-2 control-label' for='email'>Email</label>
        <div class="col-sm-8">
          <input class="form-control" type='text' name='email' id='email' />
        </div>
      </div>

      <div class="form-group">
        <label class='col-sm-2 control-label' for='message'>Please describe the issue or suggestion</label>
        <div class="col-sm-8">
          <textarea class="form-control" name='message' id='message' rows='7'></textarea>
        </div>
      </div>

      <div class="form-group">
        <div class="col-sm-offset-2 col-sm-8">
          <button class="btn btn-primary" type="submit">Send</button>
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
