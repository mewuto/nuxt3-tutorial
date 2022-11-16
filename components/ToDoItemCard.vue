<template>
    <div>{{ name }}</div>
</template>
<script lang="ts">
import { Component, Vue, Prop } from "nuxt-property-decorator";
import { ToDoItem } from "~/types";

@Component({})
export default class ToDoItemCard extends Vue {
    @Prop({ required: true }) public toDoItem!: ToDoItem;

    public get name(): string {
        return this.toDoItem.name;
    }
}
</script>