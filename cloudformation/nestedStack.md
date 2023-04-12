# NestedSTack
Resource in
    1) Resource in nested stack have share life cycle.
    2) Stack resouce have 500 limit
    3) can not easily use resource . You can not use Ref in other stack.
    4) Roots stack can have parameter and output. 
A root stack can contain and create nested stacks .. each of which can be passed parameters and provide back outputs.

Nested stacks should be used when the resources being provisioned share a lifecycle and are related.