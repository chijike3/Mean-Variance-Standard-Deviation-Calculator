# Mean-Variance-Standard-Deviation-Calculator
def calculate(np_list) :
    if len(np_list) < 9:
        raise ValueError("List must contain nine numbers." )
    
    reshaped_array = np.reshape(np_list,(3,3))
    column_axis_sum = np.sum(reshaped_array, axis=0)
    ctl= column_axis_sum.tolist()
    
    row_axis_sum = np.sum(reshaped_array, axis = 1)
    rtl= row_axis.tolist()
    
    flat_sum = np.sum(reshaped_array)
    
    sum_list = []
    sum_list.append(ctl)
    sum_list.append(rtl)
    sum_list.append(flat_sum)
    
    
    column_axis_var = np.var(reshaped_array, axis=0)
    cvl = column_axis_var.tolist()
    
    row_axis_var = np.var(reshaped_array, axis = 1)
    rvl = row_axis_var.tolist()
    
    flat_var = np.var(reshaped_array)
    
    var_list = []
    var_list.append(cvl)
    var_list.append(rvl)
    var_list.append(flat_var)
    
    
    column_axis_std = np.std(reshaped_array, axis =0)
    csl = column_axis_std.tolist()
    
    row_axis_std = np.std(reshaped_array,axis =1)
    rsl = row_axis_std.tolist()
    
    flat_std = np.std(reshaped_array)
    
    std_list = []
    std_list.append(csl)
    std_list.append(rsl)
    std_list.append(flat_std)
    
    
    column_axis_mean = np.mean(reshaped_array, axis =0)
    cml = column_axis_mean.tolist()
    
    row_axis_mean = np.mean(reshaped_array,axis =1)
    rml = row_axis_mean.tolist()
    
    flat_mean = np.mean(reshaped_array)
    
    mean_list = []
    mean_list.append(cml)
    mean_list.append(rml)
    mean_list.append(flat_mean)
    
    
    column_axis_max = np.amax(reshaped_array, axis =0)
    cmaxl = column_axis_max.tolist()
    
    row_axis_max = np.amax(reshaped_array,axis =1)
    rmaxl = row_axis_max.tolist()
    
    flat_max = np.amax(reshaped_array)
    
    max_list = []
    max_list.append(cmaxl)
    max_list.append(rmaxl)
    max_list.append(flat_max)
    
    column_axis_min = np.amin(reshaped_array, axis =0)
    cminl = column_axis_min.tolist()
    
    
    row_axis_min = np.amin(reshaped_array,axis =1)
    rminl = row_axis_min.tolist()
    
    flat_min = np.amin(reshaped_array)
    
    
    min_list = []
    min_list.append(cminl)
    min_list.append(rminl)
    min_list.append(flat_min)
    
    
    
    result_dict = {}
    result_dict['mean'] = mean_list
    result_dict['variance'] = var_list
    result_dict['standard deviation'] = std_list
    result_dict['max'] = max_list
    result_dict['min'] = min_list
    result_dict['sum'] = sum_list

    return result_dict
