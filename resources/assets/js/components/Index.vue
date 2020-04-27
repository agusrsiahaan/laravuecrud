<template>
    <div class="card">
        <div class="card-header">
            <router-link to="/create" class="btn btn-info float-right">Create New Post</router-link>
        </div>
        <div class="card-body">
            <table class="table table-bordered">
                <thead>
                <tr>
                    <th>Title</th>
                    <th>Description</th>
                    <th width="110"></th>
                    <th width="100"></th>
                    <th width="120"></th>
                </tr>
                </thead>
                <tbody>
                <tr>
                    <td>John</td>
                    <td>Doe</td>
                    <td><button class="btn btn-info"><i class="fa fa-eye"></i> View</button></td>
                    <td><button class="btn btn-warning"><i class="fa fa-pencil-square-o"></i> Edit</button></td>
                    <td><button class="btn btn-danger"><i class="fa fa-trash"></i> Delete</button></td>
                </tr>
             
                </tbody>
            </table>
        </div>
    </div>
</template>