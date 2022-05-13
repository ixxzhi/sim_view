<template>
  <el-container>
    <el-card>
      <el-form>
        <el-form-item
          prop="email"
          label="邮箱"
          :rules="[
      { required: true, message: '请输入邮箱地址', trigger: 'blur' },
      { type: 'email', message: '请输入正确的邮箱地址', trigger: ['blur', 'change'] }
    ]"
        >
          <el-input v-model="user.email"></el-input>
        </el-form-item>
      </el-form>
    </el-card>
  </el-container>
</template>

<script>
export default {
  name: 'Register',
  data () {
    return {
      user: {
        email: ''
      }
    }
  }
}
</script>

<style scoped>

</style>
