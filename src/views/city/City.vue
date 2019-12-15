<template>
<div>
    <city-header></city-header>
    <city-search :cities="cities"></city-search>
    <city-list :cities="cities" :hot="hotCities" :letter='letter'></city-list>
    <city-alphabet :cities="cities" @change='handleletterChange'></city-alphabet>
</div>
</template>

<script>
import axios from 'axios';
import CityHeader from './components/Header'
import CitySearch from './components/search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
export default {
    name: 'City',
    components:{
        CityHeader,
        CitySearch,
        CityList,
        CityAlphabet
    },
    methods:{
        async getCityInfo(){
            let res = await axios.get('/static/mock/city.json');
            res=res.data;
            if(res.ret&& res.data){
                const data = res.data;
                this.cities=data.cities;
                this.hotCities=data.hotCities;
            }
        },
        handleletterChange(letter){
            this.letter=letter;
        }
    },
    mounted(){
        this.getCityInfo();
    },
    data(){
        return {
            cities:{},
            hotCities:[],
            letter:''
        }
    }
}
</script>

<style lang="stylus" scoped>

</style>