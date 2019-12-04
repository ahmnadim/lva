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
                <form>
                    <div class="form-group">
                    <label for="name">Name</label>
                    <input type="email" class="form-control" id="name" placeholder="Enter name">
                    
                  </div>
                  <div class="form-group">
                    <label for="email">Email address</label>
                    <input type="email" class="form-control" id="email" placeholder="Enter email">
                    
                  </div>
                  <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" class="form-control" id="password" placeholder="Password">
                  </div>
                  <div class="form-group">
                      <label for="user_type">User Type</label>
                      <select class="form-control" id="user_type">
                        <option>Admin</option>
                        <option>User</option>
                        <option>Author</option>
                      </select>
                    </div>
                  <div class="form-group form-check">
                    <input type="checkbox" class="form-check-input" id="exampleCheck1">
                    <label class="form-check-label" for="exampleCheck1">Check me out</label>
                  </div>
                </form>
              </div>
              <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-dismiss="modal">Cencel</button>
                <button type="button" class="btn btn-primary">Add</button>
              </div>
            </div>
          </div>
        </div>


    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
