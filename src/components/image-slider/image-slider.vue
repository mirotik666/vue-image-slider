<script> 
export default {
    component:{},
    props:{
        image: Array 
    },
    data(){
        return{
            index: 0
        };
    },
    computed:{
        length(){
            return 3;
        },
        canGoNext(){
             return  this.index <  this.lenght - 1;
        },
        canGoPrev(){
             return  this.index > 0;
        },
        leftPosition(){
            const unit = '%';
            const left = -100 * this.index;
            return left + unit;
        }
    },
    methods:{
        prev () {
            if(!canGoPrev) return;
            this.index -=1;
       },
        next () {
            if(!canGoNext) return;
            this.index +=1;

        }
    }
};
</script>
 <style src= './image-slider.css'/>

<template>
 <div class ="component-image-slider">
         <div class = "slides">
                <picture v-bind:style="{ left: leftPosition }" class="slide" >
                 <img src= "http://res.cloudinary.com/constgen/image/upload/w_600,h_470,c_fill/Cars/1411800820_nissangt-r_wm_carreveal_week6_forzahorizon21.jpg" alt="">
                     </picture>
                 <picture class="slide">
                     <img src= "http://res.cloudinary.com/constgen/image/upload/w_600,h_470,c_fill/Cars/ChevroletCorvetteZO6_MayDLC_ForzaHorizon2_01_WM.jpg" alt="">
                </picture>
                 <picture class="slide">
                 <img src= "http://res.cloudinary.com/constgen/image/upload/w_600,h_470,c_fill/Cars/14442c5e-1063-48d9-9850-537615e0333a.jpg.jpg" alt="">
                    </picture>
                
         </div>
         <button @click="prev" class="prev">&#100094;</button>
         <button @click="next" class="next">&#100095; </button>
 </div>

</template>

