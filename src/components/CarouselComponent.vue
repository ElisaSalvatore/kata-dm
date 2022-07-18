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
                <h6><strong>Sophie Hall</strong></h6>
                <p> <strong>Founder, Catalog</strong> </p>
                <p>Web Design Agency</p>
            </div>

            <div class="bottom-details pr">
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

    }
}
</script>

<style lang="scss" scoped>
@import '@/scss/variables.scss';

#carousel-container {
    max-height: 600px;

    .pr {
        position: relative;
    }

    .component {
        max-height: 600px;

        img {
            width: 100%;
            max-height: 600px;
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
            bottom: 5%;
            left: 50px;
            color: $white;
            text-align: start;

            p {
                font-size: 9px;
                margin: 0;
            }

        }

        .bottom-details {
            position: absolute;
            bottom: 30px;
            right: 50px;

            button {
                cursor: pointer;
                border: 0.5px solid $white;
                border-radius: 50px;
                padding: 8px 10px;
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