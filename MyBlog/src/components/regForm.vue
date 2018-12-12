<template>
    <div class="login-form">
      <div class="g-form">
        <div class="g-form-line">
          <span class="g-form-label">用户名：</span>
          <div class="g-form-input" >
            <input type="text" v-model="this.username" placeholder="请输入用户名"/>
          </div>
        </div>
        <div class="g-form-line">
          <span class="g-form-label">密码：</span>
          <div class="g-form-input" >
            <input type="password" v-model="this.password" placeholder="请输入密码"/>
          </div>
        </div>
        <div class="g-form-line">
          <span class="g-form-label">确认密码：</span>
          <div class="g-form-input" >
            <input type="password" v-model="this.repassword" placeholder="请再次确认密码"/>
          </div>
        </div>
        <div class="g-form-line">
          <div class="g-form-btn">
            <a class="button" @click="onLogin">注册</a>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
  export default {
        name: "regForm",
    props: {
      'isShow':'boolean'
    },
    data () {
          return {
            username:'',
            password:'',
            repassword:'',
          }
    },
    computed: {
          userErrors() {
            let status, errorText
            if(!/@/g.test(this.usernameModel)) {
              status = false
              errorText = '必须包含@'
            }else  {
              status = true
              errorText = ''
            }
            return {
              status,
              errorText
            }
          },
      passwordErrors () {
        let status, errorText
        if (!/@/g.test(this.usernameModel)) {
          status = false
          errorText = '必须包含@'
        }
        else {
          status = true
          errorText = ''
        }
        return {
          status,
          errorText
        }
      }
    },
    methods: {
          closerMyself () {
            this.$emit('on-close')
          }
    }
    }
</script>

<style scoped>


  .dialog-wrap {
    position: fixed;
    width: 100%;
    height: 100%;

  }

  .dialog-cover {
    background: #000;
    opacity: .3;
    position: fixed;
    z-index: 5;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  .dialog-content {
    width: 50%;
    position: fixed;
    max-height: 50%;
    overflow: auto;
    background: #fff;
    top: 20%;
    left: 50%;
    margin-left: -25%;
    z-index: 10;
    border: 2px solid #464068;
    padding: 2%;
    line-height: 1.6;
  }
  .dialog-close {
    position: absolute;
    right: 5px;
    top: 5px;
    width: 20px;
    height: 20px;
    text-align: center;
    cursor: pointer;
  }
  .dialog-close:hover {
    color: #4fc08d;
  }

</style>
