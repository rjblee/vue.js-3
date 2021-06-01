<template>
  <div>
    <pre
      >{{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <form @submit="submitForm">
    <div>
      <label for="name">Name</label><br />
      <input type="text" id="name" v-model="formValues.name" />
    </div>
    <br />
    <div>
      <label for="profile">Profile Summary</label><br />
      <textarea
        name=""
        id="profile"
        v-model="formValues.profileSummary"
        cols="30"
        rows="10"
      ></textarea>
    </div>
    <br />
    <div>
      <label for="country">Country</label><br />
      <select id="country" v-model="formValues.country">
        <option value="">Select a Country</option>
        <option value="canada">Canada</option>
        <option value="korea">Korea</option>
        <option value="korea">Australia</option>
        <option value="usa">USA</option>
      </select>
    </div>
    <br />
    <div>
      <label for="job-location">Job Location</label><br />
      <select multiple id="job-location" v-model="formValues.jobLocation">
        <option value="canada">Canada</option>
        <option value="korea">Korea</option>
        <option value="australia">Australia</option>
        <option value="usa">USA</option>
      </select>
    </div>
    <br />
    <div>
      <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" />
      <label for="remoteWork">Open to remote work?</label>
    </div>
    <br />
    <div>
      <label for="remoteWork">Skill Set</label><br />
      <input
        type="checkbox"
        id="html"
        value="html"
        v-model="formValues.skillSet"
      />
      <label for="html">HTML</label>
      <input
        type="checkbox"
        id="css"
        value="css"
        v-model="formValues.skillSet"
      />
      <label for="css">CSS</label>
      <input
        type="checkbox"
        id="javascript"
        value="javascript"
        v-model="formValues.skillSet"
      />
      <label for="javascript">JavaScript</label>
      <input
        type="checkbox"
        id="vue"
        value="vue"
        v-model="formValues.skillSet"
      />
      <label for="vue">Vue</label>
    </div>

    <div>
      <button>Submit</button>
    </div>
  </form>
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
        remoteWork: false,
        skillSet: [],
        yearsOfExperience: "",
      },
    };
  },
  methods: {
    submitForm() {
      event.preventDefault();
      console.log("Form Values", this.formValues);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir;
  text-align: center;
  margin-top: 60px;
}
</style>
