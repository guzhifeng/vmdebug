# Here are  some tool commands for reference.

Here are  some tool commands for reference.

## define the vm
virsh define vmdebug.xml

## start the vm
virsh start vmdebug

## check the tc rules
tc class ls dev $tap

## migrate
target_node=NODE_ADDR virsh migrate --live vmdebug qemu+tcp://${target_node}/system --compressed --verbose  --unsafe --tunnelled --p2p

## stop the vm
virsh destroy vmdebug

## undefine the vm
virsh undefine vmdebug

