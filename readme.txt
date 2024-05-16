esper-pkpy

esper python ECS ported to pocketpy (pkpy)

https://github.com/benmoran56/esper/
https://github.com/pocketpy/pocketpy

get pocketpy...
https://github.com/pocketpy/pocketpy/archive/refs/tags/v1.4.5.zip

build pocketpy shell...
pip install cmake
python cmake_build.py

run pocketpy tests...
python scripts/run_tests.py

test the pocketpy shell (type "exit()" and then ENTER to exit)...
<path-to-pocketpy>/build/Release/main.exe

run esper-pkpy tests...
<path-to-pocketpy>/build/Release/main.exe ./test_world.py

make esper available as an imported module...
in cpp: vm->_lazy_modules["esper"] = "<contents of esper.py>";
in py: import esper

warning...
esper's event 'handler' system uses weakref system to auto unsubscribe objects.  This isn't
available in pkpy so please make use of the manual unsubscription with remove_handler instead

At time of writing, beyond the test_world.py tests, this hasn't been extensively tested
