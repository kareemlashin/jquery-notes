 let count =1;
            $("#addform").click(function () {
                $('#dynamic-form').append(`
                  <div class="row mx-3 new-form">
                            <div class="col-lg-6 col-md-6 col-sm-12 form-group">
                                <label>name arabic</label>
                                <input type="text" name="name_ar[]" >
                            </div>
                            <div class="col-lg-6 col-md-6 col-sm-12 form-group">
                                <label>name english</label>
                                <input type="text" name="name_en[]" >
                            </div>
                            <div class="col-lg-6 col-md-6 col-sm-12 form-group">
                                <label>description arabic</label>
                                <input type="text" name="description_ar[]" >
  </div>
                            <div class="col-lg-6 col-md-6 col-sm-12 form-group">
                                <label>name english</label>
                                <input type="text" name="description_en[]" >
                            </div>
                            <div class="col-lg-6 col-md-6 col-sm-12 form-group">
                                <label>start date</label>
                                <input type="date" name="start_date[]" >
                            </div>
                            <div class="col-lg-6 col-md-6 col-sm-12 form-group">
                                <label>end date</label>
                                <input type="date" name="end_date[]" >
                            </div>
                            <button id="removeRow"  class="btn btn-rounded theme-btn-two px-5 removeForm">remove form</button>
                  </div>
               `)
                count++;
            });
            $(document).on('click', '#removeRow', function () {
                $(this).closest('.new-form').remove();
                count--;
            })
