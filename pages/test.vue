<template>
  <div class="row">
    <div class="col-6">
      <div>
        <b-button>Button</b-button>
        <b-button variant="danger">Button</b-button>
        <b-button variant="success">Button</b-button>
        <b-button variant="outline-primary">Button</b-button>
      </div>
    </div>
    <div class="col-6">
      <a-button-group>
        <a-button>Cancel</a-button>
        <a-button type="primary">OK</a-button>
      </a-button-group>
      <a-button-group>
        <a-button disabled>L</a-button>
        <a-button disabled>M</a-button>
        <a-button disabled>R</a-button>
      </a-button-group>
      <a-button-group>
        <a-button type="primary">L</a-button>
        <a-button>M</a-button>
        <a-button>M</a-button>
        <a-button type="dashed">R</a-button>
      </a-button-group>

      <h4>With Icon</h4>
      <a-button-group>
        <a-button type="primary"> <a-icon type="left" />Go back </a-button>
        <a-button type="primary"> Go forward<a-icon type="right" /> </a-button>
      </a-button-group>
      <a-button-group>
        <a-button type="primary" icon="cloud" />
        <a-button type="primary" icon="cloud-download" />
      </a-button-group>
    </div>
    <div class="col-12">
      <a-popconfirm
        title="Are you sure delete this task?"
        ok-text="Yes"
        cancel-text="No"
        @confirm="confirm"
        @cancel="cancel"
      >
        <a href="#">Delete</a>
      </a-popconfirm>
    </div>
    <a-divider orientation="left">Left Text</a-divider>
    <div class="col-12">
      <a-collapse default-active-key="1" :bordered="false">
        <a-collapse-panel key="1" header="This is panel header 1">
          <p>{{ text }}</p>
        </a-collapse-panel>
        <a-collapse-panel
          key="2"
          header="This is panel header 2"
          :disabled="false"
        >
          <p>{{ text }}</p>
        </a-collapse-panel>
        <a-collapse-panel key="3" header="This is panel header 3">
          <p>{{ text }}</p>
        </a-collapse-panel>
      </a-collapse>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: `A dog is a type of domesticated animal.Known for its loyalty and faithfulness,it can be found as a welcome guest in many households across the world.`
    }
  },
  methods: {
    confirm(e) {
      //   console.log(e)
      this.$message.success('Click on Yes')
    },
    cancel(e) {
      //   console.log(e)
      this.$message.error('Click on No')
    }
  }
}
</script>

<style></style>
