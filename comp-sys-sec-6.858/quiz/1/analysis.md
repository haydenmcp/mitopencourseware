# Quiz 1 Problem Analysis

Ben Bitdiddle is building a web server that runs the following code sequence, in which process_req()
is invoked with a user-supplied string of arbitrary length. Assume that process_get() is safe, and for
the purposes of this question, simply returns right away.

```cplusplus
void process_req(char *input) {

char buf[256];

strcpy(buf, input);

if (!strncmp(buf, "GET ", 4))

process_get(buf);

return;

}
```

1. [6 points]: Ben Bitdiddle wants to prevent attackers from exploiting bugs in his server, so he
decides to make the stack memory non-executable. Explain how an attacker can still exploit a buffer
overflow in his code to delete files on the server. Draw a stack diagram to show what locations on the
stack you need to control, what values you propose to write there, and where in the input string these
values need to be located. 
