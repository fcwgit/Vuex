<template>
    <div>
        <h2>{{msg}}</h2>
        <hr/>
        <!-- <h3>{{$store.state.count}}</h3> -->
        <head>{{$store.state.count}}</head>
    </div>
    
</template>

<script>
    import store from '../vuex/store';
    // export default {
    //     data(){
    //         return{
    //             msg:'Hello  Vuex '
    //         }
    //     },
    //     store
    // }

    export default {
        name: 'Count',
        data () {
            return {
                msg: 'Hello Vuex'
            }
        },
        store
    }
</script>
