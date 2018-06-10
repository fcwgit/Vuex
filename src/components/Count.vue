<template>
    <div>
        <h2>{{msg}}</h2>
        <hr/>
        <h3>{{$store.state.count}} - {{count}}</h3>
        <p>
            <!-- <button @click="$store.commit('add',10)">add</button> -->
            <!-- <button @click="$store.commit('reduce')">reduce</button> -->
            <button @click="add(10)">add</button>
            <button @click="reduce('')">reduce</button>
        </p>
    </div>
    
</template>

<script>
    import store from '@/vuex/store';
    import {mapState,mapMutations,mapGetters} from 'vuex'
    export default {
        data(){
            return{
                msg:'Hello  Vuex '
            }
        },
        // computed:{
        //     countt(){
        //         return this.$store.state.count;
        //     }
        // },
        // computed:mapState({
        //     count:state=>state.count
        // }),
        // computed:mapState(['count']),
        computed:{
            ...mapState['count'],
            count(){
                return this.$store.getters.count;
            }
            // ...mapGetters['count']
        },
        methods:mapMutations(['add','reduce']),
        store
    }

    
</script>
