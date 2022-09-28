# Integrating Business Content with Content federation

There are two ways for integrating business content: You can either create applications manually using the tools described in the administration section or consume large amounts of content in a more efficient way with content federation. To do so, content administrators on provider side (e.g. in the S/4HANA system) need to configure the applications and the content structure and then select the roles that should be exposed to SAP Build Work Zone. The Work Zone administrator sets up connectivity with the provider system, selects the content from the provider system and manages role assignments to users and sites.



## Level 2 Heading

After completing these steps you will have....

1.	Click here.
<br>![](/exercises/ex0/images/00_00_0010.png)

2.	Insert this code.
``` abap
 DATA(params) = request->get_form_fields(  ).
 READ TABLE params REFERENCE INTO DATA(param) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.
```

## Summary

Now that you have ... 
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)
