<template>
    <div>
        <h3 class="text-sm uppercase tracking-wide text-gray-600 bg-gray-200 p-3">{{ filter.name }}</h3>

        <div class="p-2">
            <label class="block items-center"
                   v-for="(option, index) in filter.options"
                   :key="index"
                   :class="{
                      'inline-flex': filter.horizontal,
                      'ml-4': (index > 0 && filter.horizontal),
                      'mt-2': (index > 0 && !filter.horizontal)
                   }"
            >
                <input type="radio"
                       class="form-radio"
                       v-model="value"
                       :value="option.value"
                       @change="onChange"
                >
                <span class="ml-2">{{ option.name }}</span>
            </label>
        </div>
    </div>
</template>
