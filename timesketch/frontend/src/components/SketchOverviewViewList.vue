<!--
Copyright 2019 Google Inc. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->
<template>
  <div>
    <ul class="content-list">
      <li style="padding:10px;border-bottom:none;" v-for="view in views" :key="view.id">
        <router-link :to="{ name: 'SketchExplore', query: {view: view.id}}"><strong>{{ view.name }}</strong></router-link>
        <br>
        <span class="is-size-7">
          Created {{ view.created_at | moment("YYYY-MM-DD HH:mm") }}
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ts-sketch-overview-view-list',
  props: ['views']
}
</script>

<!-- CSS scoped to this component only -->
<style scoped lang="scss"></style>
