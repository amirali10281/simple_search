<template>
    <div class="item base-card">
        <div class="item-image">
            <img src="../assets/images/sample.png" :alt="image">
            <div class="item-image-text">{{ item.picInfo }}</div>
        </div>
        <div class="item-content">
            <div class="item-title">{{ item.title }}</div>
            <div><span class="item-skills">skills you will gain: </span> <span>{{ item.description }}</span></div>
            <div style="margin-top: 20px ;">
                <span>
                    <i class="fa fa-star" style="color: gold; font-size: larger;"></i> {{ item.star }}
                </span>
                <span>
                    ({{ item.reviews }}k reviews)
                </span>
            </div>
            <div>
                <span style="font-size: xx-small ; margin-left: 5px;">{{ item.otherInfo }}</span>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    props: {
        item: {
            default: {
                title: "title",
                picInfo: "item-image-text",
                writer: "description",
                description: "description",
                image: "image",
                reviews: 4.7,
                otherInfo: 'Intermediate.Specialiation.3.6months',
                star: 5
            }
        },
    },
    methods: {

    }
}
</script>

<style scoped>
img {
    width: 100%;
    height: 100%;
}

.item-image {
    border-radius: 1rem;
    background-image: linear-gradient(to bottom right, rgb(255, 26, 232), rgb(85, 0, 164));
    ;
    width: auto;
    height: 200px;
    position: relative;
    color: transparent;
}

.item-image-text {
    position: absolute;
    bottom: 20px;
    left: 20px;
    right: 20px;
    text-align: center;
    font-size: xx-large;
    font-weight: bold;
    transition: all linear 0.2s;
}

.item-image:hover {
    color: white !important;
}

.item-content {
    padding: 10px;
}

.item-title {
    font-size: large;
    font-weight: bolder;
}

.item-skills {
    font-weight: bold;
}
</style>

