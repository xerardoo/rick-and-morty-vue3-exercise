<template>
    <div class="character">
        <img :src="character.image" :alt="character.name">
        <div class="character__info">
            <h3>{{character.name}}</h3>
            <div class="status">
                <span :class="
                character.status==='Alive' ? 'alive':
                character.status==='Dead' ? 'dead': 'default'
                ">
                </span>
                <span>{{character.status}} - {{character.species}}</span>
            </div>
            <div class="origin">
                <span>
                    Origin: {{character.origin.name}}
                </span>
            </div>
            <div class="location">
                Location: {{character.location.name}}
            </div>

        </div>
    </div>
</template>

<script>
    export default {
        name: "CardCharacter",
        props: ['character']
    }
</script>

<style scoped>

    .character {
        background-color: #24282f;
        border-radius: 20px;
        box-shadow: 0 0 10px 1px #3c3e44;
        overflow: hidden;
        cursor: pointer;
        transition: transform 200ms ease-in-out;
        height: 100%;
    }

    .character:hover {
        transform: scale(1.05);
    }

    h3 {
        color: orange;
    }

    span {
        color: gray;
    }

    h3 {
        margin-bottom: 0.5rem;
    }

    .character__info {
        padding: 1.5rem;
    }

    .character__info .status {
        display: flex;
        align-items: center;
        margin-bottom: 0.5rem;
    }

    .character__info span {
        color: gray;
    }

    .character__info span:first-child {
        width: 10px;
        height: 10px;
        border-radius: 50%;
        margin-right: 0.5rem;
    }

    .character__info .alive {
        background-color: green;
    }

    .character__info .dead {
        background-color: red;
    }

    .character__info .default {
        background-color: white;
    }

    .character__info .origen {
        margin-bottom: 0.5rem;
    }
</style>