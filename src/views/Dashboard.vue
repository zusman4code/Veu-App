<template>
  <div class="container mr-2 ">
  
      
   <b-button v-b-modal.my-modal class="dn-btn">+ New Building</b-button>
   <b-modal id="my-modal">
     <form ref="form" @submit.stop.prevent="handleSubmit">
        <b-form-group
          :state="nameState"
          label="Name"
          label-for="name-input"
          invalid-feedback="Name is required"
        >
          <b-form-input
            id="name-input"
            v-model="name"
            :state="nameState"
            required
          ></b-form-input>
        </b-form-group>
         <b-form-group
          :state="nameState"
          label="Name"
          label-for="name-input"
          invalid-feedback="Name is required"
        >
          <b-form-input
            id="name-input"
            v-model="name"
            :state="nameState"
            required
          ></b-form-input>
        </b-form-group>
         <b-form-group
          :state="nameState"
          label="Name"
          label-for="name-input"
          invalid-feedback="Name is required"
        >
          <b-form-input
            id="name-input"
            v-model="name"
            :state="nameState"
            required
          ></b-form-input>
        </b-form-group>
      </form>
   </b-modal>
    <div class="row">
      <div class="col">
        <h4 class="my-3">Building Project Sites</h4>
      </div>
    </div>
    <div class="row equal">
      <!-- <div class="col-xs-12 col-sm-6 col-md-3 d-flex pb-3" v-for="board in unarchivedBoards" :key="board.id"> -->
         <div class="col-xs-12 col-sm-6 col-md-3 d-flex pb-3"  v-for="todo of todos" :key="todo.id">
        <div class="card w-100 board-item grc-card">
          <div class="card-body">
            <div class="d-flex justify-content-between">
              <h5 class="card-title flex-nowrap">F1</h5>
              <span @click="handleTaskBoardEditing(board)">...</span>
            </div>
                  
                                                <h6 class="dp-h">Projects</h6>
                                                <hr class="mt-1">
                                                <div class="d-flex align-items-cetner justify-content-between small mb-1">
                                                    <div class="font-weight-bold">Server Setup</div>
                                                    <div class="small">25%</div>
                                                </div>
                                                <div class="progress mb-3"><div class="progress-bar bg-danger" role="progressbar" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div></div>
                                                <div class="d-flex align-items-cetner justify-content-between small mb-1">
                                                    <div class="font-weight-bold">Database Migration</div>
                                                    <div class="small">50%</div>
                                                </div>
                                                <div class="progress mb-3"><div class="progress-bar bg-warning" role="progressbar" style="width: 50%" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100"></div></div>
                                                <div class="d-flex align-items-cetner justify-content-between small mb-1">
                                                    <div class="font-weight-bold">Version Release</div>
                                                    <div class="small">75%</div>
                                                </div>
                                                <div class="progress mb-3"><div class="progress-bar bg-primary" role="progressbar" style="width: 75%" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div></div>
                                                <div class="d-flex align-items-cetner justify-content-between small mb-1">
                                                    <div class="font-weight-bold">Product Listings</div>
                                                    <div class="small">100%</div>
                                                </div>
                                                <div class="progress mb-4"><div class="progress-bar bg-success" role="progressbar" style="width: 100%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div></div>
                                                <div class="text-right">
                                                    <a class="btn btn-primary btn-sm d-btn" href="javascript:void(0);">Visit Task Center<svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-arrow-right ml-1"><line x1="5" y1="12" x2="19" y2="12"></line><polyline points="12 5 19 12 12 19"></polyline></svg></a>
                                                </div>
           
      
          
          </div>
        </div>
      </div>


    </div>
  
  </div>
</template>
<script>



import axios from 'axios';

const baseURL = "https://reqres.in/api/users?page=2"

export default {
  name: 'Dashboard',
  data() {
    return {
      todos: [],
      todoName: ''
    }
  },
  
  async created() {
    this.header= {"Access-Control-Allow-Origin ":'*'};
    try {
      const res = await axios.get(baseURL+"/projects",this.header)

      this.todos = res.data;
    } catch(e) {
      console.error(e)
    }
  },
  methods: {
    async addTodo() {
      const res = await axios.post(baseURL, { name: this.todoName })

      this.todos = [...this.todos, res.data]

      this.todoName = ''
    }
  }
}
</script>
<style scoped>
.grc-card{
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.dn-btn{
  background: #FF3F3F;
  color: blanchedalmond;
   border: transparent;
}

a.d-btn{
  background: #828283;
  color: blanchedalmond;
  padding: 6px 20px;
  border: transparent;
  
}
h4.my-3{
      border-left: 3px solid #000;
    padding-left: 7px;
}

h6.dp-h{
  color: #F92528;
    font-weight: bold;
}

</style>

