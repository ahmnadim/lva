<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-12 mt-5">
                <div class="card bg-dark">
                    <div class="card-header">
                        <i class="fas fa-list"></i> User List
                        <button type="button" class="btn btn-primary btn-sm float-right" data-toggle="modal" data-target="#exampleModalCenter"><i class="fas fa-user-plus fa-fw fa-fw"></i></button>
                    </div>

                    <div class="card-body">
                       <table class="table table-striped">
                          <thead>
                            <tr>
                              <th scope="col">#</th>
                              <th scope="col">Name</th>
                              <th scope="col">Email</th>
                              <th scope="col">Type</th>
                              <th scope="col">Status</th>
                              <th scope="col">Action</th>
                            </tr>
                          </thead>
                          <tbody>
                            <tr>
                              <th scope="row">1</th>
                              <td>Mark</td>
                              <td>Otto</td>
                              <td>Otto</td>
                              <td>Otto</td>
                              <td><button class="btn btn-primary btn-sm">Edit</button> <button class="btn btn-danger btn-sm">Delete</button></td>
                            </tr>
                          </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>

        <div class="modal fade" id="exampleModalCenter" tabindex="-1" role="dialog" aria-labelledby="exampleModalCenterTitle" aria-hidden="true">
          <div class="modal-dialog modal-dialog-centered" role="document">
            <div class="modal-content bg-dark">
              <div class="modal-header">
                <h5 class="modal-title" id="exampleModalCenterTitle">Add New User</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                  <span aria-hidden="true">&times;</span>
                </button>
              </div>
              <div class="modal-body">
                <form @submit.prevent="login" @keydown="form.onKeydown($event)" enctype="multipart/form-data">
                    <div class="form-group">
                      <label for="name">Name</label>
                      <input v-model="form.name" type="text" name="name" id="name" 
                        class="form-control" :class="{ 'is-invalid': form.errors.has('name') }">
                      <has-error :form="form" field="name"></has-error>
                    </div>
                    <div class="form-group">
                      <label for="email">E-mail</label>
                      <input v-model="form.email" type="text" name="email" id="email" 
                        class="form-control" :class="{ 'is-invalid': form.errors.has('email') }">
                      <has-error :form="form" field="email"></has-error>
                    </div>
                    <div class="form-group">
                      <label for="passowrd">Password</label>
                      <input v-model="form.passowrd" type="text" name="passowrd" id="passowrd" 
                        class="form-control" :class="{ 'is-invalid': form.errors.has('passowrd') }">
                      <has-error :form="form" field="passowrd"></has-error>
                    </div>
                    <div class="form-group">
                      <label for="type">Type</label>
                      <select v-model="form.type" type="text" name="type" id="type" 
                        class="form-control" :class="{ 'is-invalid': form.errors.has('type') }">
                            <option disabled="">Select a role</option>
                            <option>User</option>
                            <option>Admin</option>
                            <option>Author</option>
                        </select>
                      <has-error :form="form" field="type"></has-error>
                    </div>
                    <!-- <div class="form-group">
                      <label>Image</label>
                      <input v-model="form.image" type="file" name="image"
                        class="form-control" :class="{ 'is-invalid': form.errors.has('image') }">
                      <has-error :form="form" field="image"></has-error>
                    </div> -->
                 
                </form>
              </div>
              <div class="modal-footer">
                <button type="button" class="btn btn-danger" data-dismiss="modal">Cencel</button>
                <button type="button" class="btn btn-success">Add</button>
              </div>
            </div>
          </div>
        </div>


    </div>
</template>

<script>
    export default {
        data(){
            return {
                form: new Form({
                    name: '',
                    email: '',
                    passowrd: '',
                    type: ''


                })
            }
        }
    }
</script>
