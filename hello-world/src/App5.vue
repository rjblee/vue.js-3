<template>
  <div>
    <div>
      <label for="profile">Profile Summary</label>
      <textarea
        name=""
        id="profile"
        v-model="formValues.profileSummary"
        cols="30"
        rows="10"
      ></textarea>
    </div>

    <div>
      <label for="country">Country</label>
      <select name="" id="country">
        <option value="">Select a Country</option>
        <option value="canada">Canada</option>
        <option value="korea">Korea</option>
        <option value="usa">USA</option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
      },
    };
  },
  methods: {},
};
</script>

<style></style>
