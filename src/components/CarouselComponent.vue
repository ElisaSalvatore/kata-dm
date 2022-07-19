<template>
    <div id="carousel-container">
        <div class="component pr" 
            v-for="(image, index) in images" 
            :key="image" 
            :index="index"
            :currentIndex="currentIndex" v-show="currentIndex === index"
            
        >
            <img :src="image" :alt="image" />

            <h3 class="caption col-10 pr">
                We move 10x faster than our peers and stay consistent. While they're bogged down with design debt, we're
                releasing new features.
            </h3>

            <div class="infos pr">
                <h5 class="pb-2"><strong>Sophie Hall</strong></h5>
                <p class="mb-0"> <strong>Founder, Catalog</strong> </p>
                <p class="mt-0">Web Design Agency</p>
            </div>

            <div class="bottom-details pr">

                <div class="stars">
                    <img src="../assets/star.svg" alt="star">
                    <img src="../assets/star.svg" alt="star">
                    <img src="../assets/star.svg" alt="star">
                    <img src="../assets/star.svg" alt="star">
                    <img src="../assets/star.svg" alt="star">
                </div>

                <button class="prev" @click="prevImg">
                    <img src="../assets/arrow-l.svg" alt="">
                </button>

                <button class="next" @click="nextImg">
                    <img src="../assets/arrow-r.svg" alt="">
                </button>
            </div>
            
        </div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            images: [
                require("@/assets/slideshow/1.jpeg"),
                require("@/assets/slideshow/2.jpeg"),
                require("@/assets/slideshow/3.jpeg"),
            ],
            currentIndex: 0,
        }
    },
    methods: {
        nextImg() {
            this.currentIndex++;
            if (this.currentIndex >= this.images.length) {
                this.currentIndex = 0;
            }

        },
        prevImg() {
            this.currentIndex--;
            if (this.currentIndex < 0) {
                this.currentIndex = this.images.length - 1;
            }
        },
        printsStar() {
            
        }

    }
}
</script>

<style lang="scss" scoped>
@import '@/scss/variables.scss';

#carousel-container {
    width: 100%;
    
    // height: 100%;
    max-height: 800px;

    .pr {
        position: relative;
    }

    .component {
        width: 100%;        

        img {
            width: 100%;
            max-height: 650px;
            height: 100%;
            object-fit: cover;
        }

        .caption {
            position: absolute;
            bottom: calc(50% - 200px);
            left: 50px;
            color: $white;
            font-size: 21px;
            font-weight: 600;
            text-align: start;
            line-height: 30px;
            word-spacing: 5px;
        }

        .infos {
            width: 250px;
            height: 50px;
            position: absolute;
            bottom: 8%;
            left: 50px;
            color: $white;
            text-align: start;

            p {
                font-size: 12px;
            }

        }

        .bottom-details {
            position: absolute;
            bottom: 30px;
            right: 50px;

            .stars {
                display: flex;
                justify-content: end;
                padding-right: 5px;

                img {
                    width: 15px;
                    margin: 20px 0;
                }
            }

            button {
                cursor: pointer;
                border: 0.5px solid $white;
                border-radius: 50px;
                padding: 4px 6px;
                background-color: rgba(255, 255, 255, 0);

                img {
                    width: 20px;
                    height: 20px;
                }

                &:active {
                    background-color: rgba(255, 255, 255, 0.8);
                }
            }

            .prev {
                margin-right: 20px;
            }
        }
    }
}
</style>