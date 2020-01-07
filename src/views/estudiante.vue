<template>
    <div>
        <div class="container">
        <div class="columns">
            <div class="column">
            <h1>Formulario Estudiante</h1>
            </div>
        </div>
        <div class="columns">
        <div class="column">
            <label>Codigo: </label>
            <input class="input" type="text" placeholder="ingrese codigo">
            <label>Nombre: </label>
            <input class="input" type="text" placeholder="ingrese nombre">
            <label>Email: </label>
            <input class="input" type="email" placeholder="ingrese email">
            <label>Fecha: </label><br>
            <input type="date">
        </div>
        </div>
        <button class="button is-primary is-4">Guardar</button>
        <button class="button is-primary" @click="Edit()">Editar</button>
        
        <div class="columns">
            <div class="column">
            <table class="table">
                <thead>
                <tr>
                    <th>Codigo</th>
                    <th>Nombre</th>
                    <th>Email</th>
                    <th>Fecha</th>
                </tr>
                </thead>
                <tbody>
                <tr>
                    <td>
                        <input class="input" :type="form.tipo" placeholder="Ingrese text" v-if = "boll== 0">
                        <h1 v-if = "boll== 1">{{form.tipo}}</h1>
                    </td>
                    <td>Jhon</td>
                    <td>jhon199611@gmail.com</td>
                    <td>14/12/1996</td>
                </tr>
                </tbody>
            </table>
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            form:{
                id:0,
                nombre:"jesus",
                tipo:"text"
            },
            boll:1,
        }
    },
    methods:{
        Edit(){
            console.log('hola')
            if(this.boll == 0){
                this.boll=1;
            }else{
                this.boll=0;
            }
        }
    }
}
</script>