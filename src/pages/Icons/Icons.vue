<template>
<div class="row">
    <div class="col-lg-8 offset-lg-1">
        <section class="widget">
            <header>
                <h5>
                    Assign Roles
                </h5>
                <div class="widget-controls">
                    <a data-widgster="expand" title="Expand" href="#"><i class="la la-angle-up"></i></a>
                    <a data-widgster="collapse" title="Collapse" href="#"><i class="la la-angle-down"></i></a>
                    <a data-widgster="close" title="Close" href="#"><i class="la la-remove"></i></a>
                </div>
            </header>
            <div class="widget-body">
                <form id="validation-form" class="form-horizontal form-label-left" 
                    data-parsley-priority-enabled="false" novalidate="novalidate">
                    <fieldset>
                        <legend>
                        </legend>
                        <div class="form-group row">
                            <label class="control-label col-sm-3" for="basic">Simple required</label>
                            <div class="col-sm-9">
                                <input type="text" id="basic" name="basic" class="form-control" required="required">
                            </div>
                        </div>
                        <div class="form-group row">
                            <label class="control-label col-sm-3" for="basic-change">
                                Min-length On Change
                                <span class="help-block">
                                    At least 10
                                </span>
                            </label>
                            <div class="col-sm-9">
                                <input type="text" id="basic-change" name="basic-change" class="form-control"
                                    data-parsley-trigger="change" data-parsley-minlength="10" required="required">
                            </div>
                        </div>
                    </fieldset>
                    <fieldset>
                        <legend>
                            <span class="badge bg-warning mr-xs">
                                HTML5
                            </span>
                            input types supported
                        </legend>
                        <div class="form-group row">
                            <label class="control-label col-sm-3" for="email">
                                E-mail
                            </label>
                            <div class="col-sm-9">
                                <input type="email" id="email" name="email" class="form-control"
                                    data-parsley-trigger="change" data-parsley-validation-threshold="1"
                                    required="required">
                                <span class="help-block">
                                    This one is triggered even when 1 character has been input
                                </span>
                            </div>
                        </div>
                        <div class="form-group row">
                            <label class="control-label col-sm-3" for="number">
                                Number
                            </label>
                            <div class="col-sm-9">
                                <input type="text" id="number" name="number" class="form-control"
                                    data-parsley-type="number" required="required">
                            </div>
                        </div>
                        <div class="form-group row">
                            <label class="control-label col-sm-3" for="range">
                                Range
                            </label>
                            <div class="col-sm-9">
                                <input type="text" class="form-control" id="range" name="range"
                                    data-parsley-range="[10, 100]" data-parsley-trigger="change"
                                    data-parsley-validation-threshold="1" required="required">
                            </div>
                        </div>
                    </fieldset>
                    <fieldset>
                        <legend>
                            More validation
                        </legend>
                        <div class="form-group row">
                            <label class="control-label col-sm-3" for="password">
                                Password helpers
                            </label>
                            <div class="col-sm-9">
                                <input type="password" id="password" name="password" class="form-control mb-sm"
                                    data-parsley-trigger="change" data-parsley-minlength="6" required="required">
                                <input type="password" id="password-r" name="password-r" class="form-control"
                                    data-parsley-trigger="change" data-parsley-minlength="6"
                                    data-parsley-equalto="#password" required="required">
                            </div>
                        </div>
                        <div class="form-group row">
                            <label class="control-label col-sm-3" for="website">
                                Website
                            </label>
                            <div class="col-sm-9">
                                <input type="text" id="website" name="website" class="form-control"
                                    data-parsley-trigger="change" data-parsley-type="url" required="required">
                            </div>
                        </div>
                    </fieldset>
                    <div class="form-actions">
                        <button type="submit" class="btn btn-success btn-square float-right">
                            Save</button>
                        <button type="button" class="btn btn-default btn-rounded">Cancel</button>
                    </div>
                </form>
            </div>
        </section>
    </div>
</div>
</template>
