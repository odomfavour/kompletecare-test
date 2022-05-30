<template>
  <div class="container-fluid">
    <h1 class="text-primary">Update Patient Medical Record</h1>
    <p class="text-mild">
      Click the tabs to view and edit patient medical details
    </p>
    <b-card class="px-2 px-md-5 px-lg-5 my-5">
      <h5 class="mt-4 text-primary">X-Ray</h5>
      <div class="row">
        <div class="col-lg-3 col-md-4 col-12 mb-3" v-for="(sign, index) in 18" :key="index">
          <b-form-checkbox
            id="checkbox-1"
            :name="`checkbox-${index}`"
            value="accepted"
          >
            Chest
          </b-form-checkbox>
        </div>
      </div>
      <hr />
      <h5 class="mt-4 text-primary">Ultrasound Scan</h5>
      <div class="row">
        <div class="col-lg-3 col-md-4 col-12 mb-3" v-for="(sign, index) in 6" :key="index">
          <b-form-checkbox
            id="checkbox-1"
            :name="`checkbox-${index}`"
            value="accepted"
          >
            Abdomen
          </b-form-checkbox>
        </div>
      </div>
      <hr class="my-3" />
      <div class="row">
        <div class="col-md-6 mb-3">
          <b-form-group label="CT Scan">
            <b-form-select
              v-model="selected"
              :options="options"
            ></b-form-select>
          </b-form-group>
        </div>
        <div class="col-md-6 mb-3">
          <b-form-group label="MRI">
            <b-form-select
              v-model="selected"
              :options="options"
            ></b-form-select>
          </b-form-group>
        </div>
      </div>
      <div class="d-flex mt-3 justify-content-end">
        <button class="btn btn-primary">Save and Send</button>
      </div>
    </b-card>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  layout: 'dashboard',
  data() {
    return {
      selected: null,
      options: [
        { value: null, text: 'Please select an option' },
        { value: 'a', text: 'This is First option' },
        { value: 'b', text: 'Selected Option' },
        { value: { C: '3PO' }, text: 'This is an option with object value' },
        { value: 'd', text: 'This one is disabled', disabled: true },
      ],
    }
  },
}
</script>
