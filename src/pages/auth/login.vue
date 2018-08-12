<template>
  <div class="login">
    <el-card>
      <div class="card-header">Admin Login</div>
      <el-form ref="login" :model="login" label-width="120px">
        <el-form-item
          label="id"
          prop="id"
          :rules="[
            { required: true, message: 'Please input id', trigger: ['blur', 'change'] }]">
          <el-input v-model="login.id"></el-input>
        </el-form-item>
        <el-form-item
          label="password"
          prop="password"
          :rules="[
            { required: true, message: 'Please input password', trigger: ['blur', 'change'] }]">
          <el-input type="password" v-model="login.password"></el-input>
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="submitLogin('login')">Login</el-button>
          <el-button @click="resetForm('login')">Reset</el-button>
        </el-form-item>
      </el-form>
    </el-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      login: {
        id: '',
        password: ''
      }
    }
  },
  methods: {
    submitLogin(formName) {
      this.$refs[formName].validate((valid) => {
        if (valid) {
          alert(this.login);
        } else {
          console.log(this);
          return false;
        }
      });
    },
    resetForm(formName) {
      this.$refs[formName].resetFields();
    }
  }
}
</script>
