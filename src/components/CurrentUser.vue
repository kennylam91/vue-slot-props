<template>
  <div>
    <span>
      <slot :user="user" :action="action">
        {{user.lastName}}
      </slot>
    </span>
    
  </div>
</template>
<script>
export default {
  data() {
    return {
      user:{
        firstName: 'pham',
        lastName:'lam'
      }, 
      action:{
        first: 'punch'
      }
    }
  },
}
</script>