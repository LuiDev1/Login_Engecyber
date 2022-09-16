<template>
    <el-row>
        <el-col :span="24">
            <div class="LoginContainer">
                <div class="Allcontent-Inputs">

                    <div class="InputDiv">
                        <img src="../assets/user.svg" alt="User Login" class="svg-config">
                        <el-input v-model="inputUser" placeholder="Usuário"/>
                    </div>

                    <div class="InputDiv input-password">
                        <img src="../assets/lock_closed.svg" alt="Password Login" class="svg-config input-config">
                        <el-input type="password" v-model="inputPassword" placeholder="Senha" show-password class="input-config"/>
                    </div>

                    <div class="AcessContainer">
                        <a href="#" id="PasswordRec">Esqueci minha senha</a>
                        <el-button type="primary" round plain class="AcessButton">Acessar</el-button>
                    </div>

                </div>
            
                        <img src="../assets/EngLogo.png" class="CyberLogo"/>
        
            </div>
        </el-col>
    </el-row>
</template>


<script>
import { ref } from 'vue'

export default {
   setup() {
    return{
        inputUser: ref(''),
        inputPassword: ref('')
    }
   }
}
</script>

<style>

/* CORPO DO SITE */
#app{
    display:block;
    width:100%;
}

body{
    padding: 0px;
    background-image: url('../assets/BackgroundLogin.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    font-family: Arial, Helvetica, sans-serif;
}

/* FIM CORPO DO SITE */


.Allcontent-Inputs{
        display: flex;
        flex-direction: column;
        width: 500px;
}


.LoginContainer{
    display: flex;
    align-items: flex-end;
    flex-direction: row-reverse;
    justify-content: center;
    height: 500px;
}



/* CONFIGURAÇÃO DOS INPUTS E ICONS */
.InputDiv{
    display: flex;
    align-items: center;
    width: 500px;
}
/* FIM CONFIGURAÇÃO DOS INPUTS E ICONS */



.CyberLogo{
    width: 600px;
}


.input-password{
    margin-top: 15px;
}



/* CONTAINER DE ACESSO */
.AcessContainer{
    display: flex;
    align-items: center;
    margin-top: 30px;
    margin-left: 30px;
}

.AcessButton{
    width: 100px;
    margin-left: 197px;
}
/* FIM CONTAINER DE ACESSO */



/* RECUPERAÇÃO DE SENHA */
#PasswordRec{
    text-decoration: none;
    font-size: 18px;
    color: #0FAEE8;
    transition: 0.2s;
}

#PasswordRec:hover{
    color: #1A6094;
}
/* FIM RECUPERAÇÃO DE SENHA */



/* INPUT ICONS */
.svg-config{
    filter: invert(100%);
    width: 100px;
    height: 30px;
}
/* FIM INPUT ICONS */




/* MEDIA QUERY */
@media screen and (max-width: 1128px) {
    .LoginContainer{
        display: flex;
        flex-direction: column-reverse;
        align-items: center;
        justify-content: center;
        height: 700px;
    }
    
    .CyberLogo{
        margin-bottom: 40px;
        margin-left: 50px
    }

    .input-password{
        margin-top: 15px;
    }
}

@media screen and (min-width: 1128px) {
    .LoginContainer{
        display: flex;
        align-items: flex-end;
        flex-direction: row-reverse;
        justify-content: center;
        height: 500px;
        margin: 0 auto;
    }
}

/* FIM MEDIA QUERY */

</style>