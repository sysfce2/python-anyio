API reference
=============

Event loop
----------

.. autofunction:: anyio.run
.. autofunction:: anyio.get_all_backends
.. autofunction:: anyio.get_cancelled_exc_class
.. autofunction:: anyio.sleep
.. autofunction:: anyio.sleep_forever
.. autofunction:: anyio.sleep_until
.. autofunction:: anyio.current_time

Asynchronous resources
----------------------

.. autofunction:: anyio.aclose_forcefully

.. autoclass:: anyio.abc.AsyncResource

Typed attributes
----------------

.. autofunction:: anyio.typed_attribute

.. autoclass:: anyio.TypedAttributeSet
.. autoclass:: anyio.TypedAttributeProvider

Timeouts and cancellation
-------------------------

.. autofunction:: anyio.move_on_after
.. autofunction:: anyio.fail_after
.. autofunction:: anyio.current_effective_deadline

.. autoclass:: anyio.CancelScope

Task groups
-----------

.. autofunction:: anyio.create_task_group

.. autoclass:: anyio.abc.TaskGroup
.. autoclass:: anyio.abc.TaskStatus

Running code in worker threads
------------------------------

.. autofunction:: anyio.to_thread.run_sync
.. autofunction:: anyio.to_thread.current_default_thread_limiter

Running code in subinterpreters
-------------------------------

.. autofunction:: anyio.to_interpreter.run_sync
.. autofunction:: anyio.to_interpreter.current_default_interpreter_limiter

Running code in worker processes
--------------------------------

.. autofunction:: anyio.to_process.run_sync
.. autofunction:: anyio.to_process.current_default_process_limiter

Running asynchronous code from other threads
--------------------------------------------

.. autofunction:: anyio.from_thread.run
.. autofunction:: anyio.from_thread.run_sync
.. autofunction:: anyio.from_thread.check_cancelled
.. autofunction:: anyio.from_thread.start_blocking_portal

.. autoclass:: anyio.from_thread.BlockingPortal
.. autoclass:: anyio.from_thread.BlockingPortalProvider

Async file I/O
--------------

.. autofunction:: anyio.open_file
.. autofunction:: anyio.wrap_file

.. autoclass:: anyio.AsyncFile
.. autoclass:: anyio.Path

Temporary files and directories
-------------------------------

.. autofunction:: anyio.mkstemp
.. autofunction:: anyio.mkdtemp
.. autofunction:: anyio.gettempdir
.. autofunction:: anyio.gettempdirb

.. autoclass:: anyio.TemporaryFile
.. autoclass:: anyio.NamedTemporaryFile
.. autoclass:: anyio.SpooledTemporaryFile
.. autoclass:: anyio.TemporaryDirectory

Context manager mix-in classes
------------------------------

.. autoclass:: anyio.ContextManagerMixin
   :special-members: __contextmanager__

.. autoclass:: anyio.AsyncContextManagerMixin
   :special-members: __asynccontextmanager__

Streams and stream wrappers
---------------------------

.. autofunction:: anyio.create_memory_object_stream

.. autoclass:: anyio.abc.UnreliableObjectReceiveStream()
.. autoclass:: anyio.abc.UnreliableObjectSendStream()
.. autoclass:: anyio.abc.UnreliableObjectStream()
.. autoclass:: anyio.abc.ObjectReceiveStream()
.. autoclass:: anyio.abc.ObjectSendStream()
.. autoclass:: anyio.abc.ObjectStream()
.. autoclass:: anyio.abc.ByteReceiveStream
.. autoclass:: anyio.abc.ByteSendStream
.. autoclass:: anyio.abc.ByteStream
.. autoclass:: anyio.abc.Listener
.. autoclass:: anyio.abc.ObjectStreamConnectable
.. autoclass:: anyio.abc.ByteStreamConnectable

.. autodata:: anyio.abc.AnyUnreliableByteReceiveStream
.. autodata:: anyio.abc.AnyUnreliableByteSendStream
.. autodata:: anyio.abc.AnyUnreliableByteStream
.. autodata:: anyio.abc.AnyByteReceiveStream
.. autodata:: anyio.abc.AnyByteSendStream
.. autodata:: anyio.abc.AnyByteStream
.. autodata:: anyio.abc.AnyByteStreamConnectable

.. autoclass:: anyio.streams.buffered.BufferedByteReceiveStream
.. autoclass:: anyio.streams.file.FileStreamAttribute
.. autoclass:: anyio.streams.file.FileReadStream
.. autoclass:: anyio.streams.file.FileWriteStream
.. autoclass:: anyio.streams.memory.MemoryObjectReceiveStream
.. autoclass:: anyio.streams.memory.MemoryObjectSendStream
.. autoclass:: anyio.streams.memory.MemoryObjectStreamStatistics
.. autoclass:: anyio.streams.stapled.MultiListener
.. autoclass:: anyio.streams.stapled.StapledByteStream
.. autoclass:: anyio.streams.stapled.StapledObjectStream
.. autoclass:: anyio.streams.text.TextReceiveStream
.. autoclass:: anyio.streams.text.TextSendStream
.. autoclass:: anyio.streams.text.TextStream
.. autoclass:: anyio.streams.text.TextConnectable
.. autoclass:: anyio.streams.tls.TLSAttribute
.. autoclass:: anyio.streams.tls.TLSStream
.. autoclass:: anyio.streams.tls.TLSListener
.. autoclass:: anyio.streams.tls.TLSConnectable

Sockets and networking
----------------------

.. autofunction:: anyio.as_connectable
.. autofunction:: anyio.connect_tcp
.. autofunction:: anyio.connect_unix
.. autofunction:: anyio.create_tcp_listener
.. autofunction:: anyio.create_unix_listener
.. autofunction:: anyio.create_udp_socket
.. autofunction:: anyio.create_connected_udp_socket
.. autofunction:: anyio.getaddrinfo
.. autofunction:: anyio.getnameinfo
.. autofunction:: anyio.wait_readable
.. autofunction:: anyio.wait_socket_readable
.. autofunction:: anyio.wait_socket_writable
.. autofunction:: anyio.wait_writable

.. autoclass:: anyio.abc.SocketAttribute
.. autoclass:: anyio.abc.SocketStream()
.. autoclass:: anyio.abc.SocketListener()
.. autoclass:: anyio.abc.UDPSocket()
.. autoclass:: anyio.abc.ConnectedUDPSocket()
.. autoclass:: anyio.abc.UNIXSocketStream()
.. autoclass:: anyio.TCPConnectable
.. autoclass:: anyio.UNIXConnectable

Subprocesses
------------

.. autofunction:: anyio.run_process
.. autofunction:: anyio.open_process

.. autoclass:: anyio.abc.Process

Synchronization
---------------

.. autoclass:: anyio.Event
.. autoclass:: anyio.Lock
.. autoclass:: anyio.Condition
.. autoclass:: anyio.Semaphore
.. autoclass:: anyio.CapacityLimiter
.. autoclass:: anyio.ResourceGuard

.. autoclass:: anyio.LockStatistics
.. autoclass:: anyio.EventStatistics
.. autoclass:: anyio.ConditionStatistics
.. autoclass:: anyio.CapacityLimiterStatistics
.. autoclass:: anyio.SemaphoreStatistics

Operating system signals
------------------------

.. autofunction:: anyio.open_signal_receiver

Low level operations
--------------------

.. autofunction:: anyio.lowlevel.checkpoint
.. autofunction:: anyio.lowlevel.checkpoint_if_cancelled
.. autofunction:: anyio.lowlevel.cancel_shielded_checkpoint

.. autoclass:: anyio.lowlevel.RunVar

Testing and debugging
---------------------

.. autoclass:: anyio.TaskInfo
.. autoclass:: anyio.pytest_plugin.FreePortFactory
.. autofunction:: anyio.get_current_task
.. autofunction:: anyio.get_running_tasks
.. autofunction:: anyio.wait_all_tasks_blocked

Exceptions
----------

.. autoexception:: anyio.BrokenResourceError
.. autoexception:: anyio.BrokenWorkerInterpreter
.. autoexception:: anyio.BrokenWorkerProcess
.. autoexception:: anyio.BusyResourceError
.. autoexception:: anyio.ClosedResourceError
.. autoexception:: anyio.ConnectionFailed
.. autoexception:: anyio.DelimiterNotFound
.. autoexception:: anyio.EndOfStream
.. autoexception:: anyio.IncompleteRead
.. autoexception:: anyio.TypedAttributeLookupError
.. autoexception:: anyio.WouldBlock
