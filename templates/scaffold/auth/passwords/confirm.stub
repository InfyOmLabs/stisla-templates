@extends('layouts.auth_app')
@section('title')
    Confirm Password
@endsection
@section('content')
    <div class="card card-primary">
        <div class="card-header"><h4>Confirm Password</h4></div>

        <div class="card-body">
            @if (session('status'))
                <div class="alert alert-success">
                    {{ session('status') }}
                </div>
            @endif
          <form method="POST" action="{{ route('password.confirm') }}">
           @csrf
               <div class="input-group mb-3">
                   <input type="password"
                          name="password"
                          class="form-control @error('password') is-invalid @enderror"
                          placeholder="Password"
                          required autocomplete="current-password">
                   <div class="input-group-append">
                       <div class="input-group-text"><span class="fas fa-lock"></span></div>
                   </div>
                   @error('password')
                   <span class="error invalid-feedback">{{ $message }}</span>
                   @enderror
               </div>

               <div class="row">
                   <div class="col-12">
                       <button type="submit" class="btn btn-primary btn-block">Confirm Password</button>
                   </div>
                   <!-- /.col -->
               </div>
           </form>
        </div>
    </div>
    <div class="mt-5 text-muted text-center">
         <a href="{{ route('password.request') }}">Forgot Your Password?</a>
    </div>
@endsection