# api documentation for  [pmx (v1.1.0)](https://github.com/keymetrics/pmx#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-pmx.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pmx) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pmx.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pmx)
#### PM2/Keymetrics advanced API

[![NPM](https://nodei.co/npm/pmx.png?downloads=true)](https://www.npmjs.com/package/pmx)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pmx/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-pmx_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pmx/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pmx/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pmx/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Keymetrics I/O"
    },
    "bugs": {
        "url": "https://github.com/keymetrics/pmx/issues"
    },
    "dependencies": {
        "debug": "^2.6",
        "json-stringify-safe": "^5.0",
        "vxx": "^1.1.1"
    },
    "description": "PM2/Keymetrics advanced API",
    "devDependencies": {
        "express": "*",
        "mocha": "*",
        "mongoose": "*",
        "nssocket": "*",
        "pm2": "github:unitech/pm2#development",
        "pm2-axon": "*",
        "request": "*",
        "shelljs": "*",
        "should": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "381d291eedd96b81a098a5c5f0df548047258ffd",
        "tarball": "https://registry.npmjs.org/pmx/-/pmx-1.1.0.tgz"
    },
    "gitHead": "2036e38dd4325fbefba6a51e87466136e0834078",
    "homepage": "https://github.com/keymetrics/pmx#readme",
    "keywords": [
        "cli",
        "fault tolerant",
        "sysadmin",
        "tools",
        "pm2",
        "logs",
        "log",
        "json",
        "express",
        "hapi",
        "kraken",
        "reload",
        "microservice",
        "programmatic",
        "harmony",
        "node-pm2",
        "production",
        "keymetrics",
        "node.js monitoring",
        "strong-pm",
        "deploy",
        "deployment",
        "daemon",
        "supervisor",
        "nodemon",
        "pm2.io",
        "ghost",
        "ghost production",
        "monitoring",
        "process manager",
        "forever",
        "profiling",
        "probes",
        "process-metrics",
        "process metrics",
        "metrics",
        "custom actions",
        "forever-monitor",
        "keep process alive",
        "process configuration",
        "clustering",
        "cluster cli",
        "cluster",
        "cron",
        "devops",
        "dev ops"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "tknew",
            "email": "strzelewicz.alexandre@gmail.com"
        }
    ],
    "name": "pmx",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/keymetrics/pmx.git"
    },
    "scripts": {
        "test": "DEBUG='axm:*' mocha test/*.mocha.js"
    },
    "version": "1.1.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pmx](#apidoc.module.pmx)
1.  boolean <span class="apidocSignatureSpan">pmx.</span>_started
1.  [function <span class="apidocSignatureSpan">pmx.</span>_interpretError (err)](#apidoc.element.pmx._interpretError)
1.  [function <span class="apidocSignatureSpan">pmx.</span>action (action_name, opts, fn)](#apidoc.element.pmx.action)
1.  [function <span class="apidocSignatureSpan">pmx.</span>catchAll (opts)](#apidoc.element.pmx.catchAll)
1.  [function <span class="apidocSignatureSpan">pmx.</span>catchPorts ()](#apidoc.element.pmx.catchPorts)
1.  [function <span class="apidocSignatureSpan">pmx.</span>catchTraffic ()](#apidoc.element.pmx.catchTraffic)
1.  [function <span class="apidocSignatureSpan">pmx.</span>configureModule (opts)](#apidoc.element.pmx.configureModule)
1.  [function <span class="apidocSignatureSpan">pmx.</span>detectV8Profiler (cb)](#apidoc.element.pmx.detectV8Profiler)
1.  [function <span class="apidocSignatureSpan">pmx.</span>emit (name, data)](#apidoc.element.pmx.emit)
1.  [function <span class="apidocSignatureSpan">pmx.</span>enableProbe (custom_namespace)](#apidoc.element.pmx.enableProbe)
1.  [function <span class="apidocSignatureSpan">pmx.</span>enableProbes (custom_namespace)](#apidoc.element.pmx.enableProbes)
1.  [function <span class="apidocSignatureSpan">pmx.</span>exposeProfiling (pmx, profiler_path)](#apidoc.element.pmx.exposeProfiling)
1.  [function <span class="apidocSignatureSpan">pmx.</span>expressErrorHandler ()](#apidoc.element.pmx.expressErrorHandler)
1.  [function <span class="apidocSignatureSpan">pmx.</span>getConf ()](#apidoc.element.pmx.getConf)
1.  [function <span class="apidocSignatureSpan">pmx.</span>getEnv ()](#apidoc.element.pmx.getEnv)
1.  [function <span class="apidocSignatureSpan">pmx.</span>getPID (file)](#apidoc.element.pmx.getPID)
1.  [function <span class="apidocSignatureSpan">pmx.</span>http (opts)](#apidoc.element.pmx.http)
1.  [function <span class="apidocSignatureSpan">pmx.</span>init (opts)](#apidoc.element.pmx.init)
1.  [function <span class="apidocSignatureSpan">pmx.</span>initModule (opts, cb)](#apidoc.element.pmx.initModule)
1.  [function <span class="apidocSignatureSpan">pmx.</span>notify (err)](#apidoc.element.pmx.notify)
1.  [function <span class="apidocSignatureSpan">pmx.</span>probe ()](#apidoc.element.pmx.probe)
1.  [function <span class="apidocSignatureSpan">pmx.</span>resolvePidPaths (filepaths)](#apidoc.element.pmx.resolvePidPaths)
1.  [function <span class="apidocSignatureSpan">pmx.</span>scopedAction (action_name, fn)](#apidoc.element.pmx.scopedAction)
1.  [function <span class="apidocSignatureSpan">pmx.</span>stopProbe ()](#apidoc.element.pmx.stopProbe)
1.  [function <span class="apidocSignatureSpan">pmx.</span>stopProbes ()](#apidoc.element.pmx.stopProbes)
1.  [function <span class="apidocSignatureSpan">pmx.</span>tracing (pmx, opts)](#apidoc.element.pmx.tracing)
1.  [function <span class="apidocSignatureSpan">pmx.</span>v8Profiling (pmx)](#apidoc.element.pmx.v8Profiling)
1.  object <span class="apidocSignatureSpan">pmx.</span>AVAILABLE_AGG_TYPES
1.  object <span class="apidocSignatureSpan">pmx.</span>AVAILABLE_MEASUREMENTS
1.  object <span class="apidocSignatureSpan">pmx.</span>Probe
1.  object <span class="apidocSignatureSpan">pmx.</span>_pmx_conf
1.  object <span class="apidocSignatureSpan">pmx.</span>_var
1.  object <span class="apidocSignatureSpan">pmx.</span>actions
1.  object <span class="apidocSignatureSpan">pmx.</span>common
1.  object <span class="apidocSignatureSpan">pmx.</span>configuration
1.  object <span class="apidocSignatureSpan">pmx.</span>events
1.  object <span class="apidocSignatureSpan">pmx.</span>monitor
1.  object <span class="apidocSignatureSpan">pmx.</span>network
1.  object <span class="apidocSignatureSpan">pmx.</span>transaction
1.  string <span class="apidocSignatureSpan">pmx.</span>default_aggregation

#### [module pmx.Probe](#apidoc.module.pmx.Probe)
1.  boolean <span class="apidocSignatureSpan">pmx.Probe.</span>_started
1.  [function <span class="apidocSignatureSpan">pmx.Probe.</span>probe ()](#apidoc.element.pmx.Probe.probe)
1.  object <span class="apidocSignatureSpan">pmx.Probe.</span>AVAILABLE_AGG_TYPES
1.  object <span class="apidocSignatureSpan">pmx.Probe.</span>AVAILABLE_MEASUREMENTS
1.  object <span class="apidocSignatureSpan">pmx.Probe.</span>_var
1.  string <span class="apidocSignatureSpan">pmx.Probe.</span>default_aggregation

#### [module pmx.actions](#apidoc.module.pmx.actions)
1.  [function <span class="apidocSignatureSpan">pmx.actions.</span>action (action_name, opts, fn)](#apidoc.element.pmx.actions.action)
1.  [function <span class="apidocSignatureSpan">pmx.actions.</span>scopedAction (action_name, fn)](#apidoc.element.pmx.actions.scopedAction)

#### [module pmx.common](#apidoc.module.pmx.common)
1.  [function <span class="apidocSignatureSpan">pmx.common.</span>getDate ()](#apidoc.element.pmx.common.getDate)

#### [module pmx.configuration](#apidoc.module.pmx.configuration)
1.  [function <span class="apidocSignatureSpan">pmx.configuration.</span>configureModule (opts)](#apidoc.element.pmx.configuration.configureModule)
1.  [function <span class="apidocSignatureSpan">pmx.configuration.</span>getPID (file)](#apidoc.element.pmx.configuration.getPID)
1.  [function <span class="apidocSignatureSpan">pmx.configuration.</span>init (conf, do_not_tell_pm2)](#apidoc.element.pmx.configuration.init)
1.  [function <span class="apidocSignatureSpan">pmx.configuration.</span>resolvePidPaths (filepaths)](#apidoc.element.pmx.configuration.resolvePidPaths)

#### [module pmx.events](#apidoc.module.pmx.events)
1.  [function <span class="apidocSignatureSpan">pmx.events.</span>emit (name, data)](#apidoc.element.pmx.events.emit)

#### [module pmx.monitor](#apidoc.module.pmx.monitor)
1.  [function <span class="apidocSignatureSpan">pmx.monitor.</span>enableProbe (custom_namespace)](#apidoc.element.pmx.monitor.enableProbe)
1.  [function <span class="apidocSignatureSpan">pmx.monitor.</span>enableProbes (custom_namespace)](#apidoc.element.pmx.monitor.enableProbes)
1.  [function <span class="apidocSignatureSpan">pmx.monitor.</span>stopProbe ()](#apidoc.element.pmx.monitor.stopProbe)
1.  [function <span class="apidocSignatureSpan">pmx.monitor.</span>stopProbes ()](#apidoc.element.pmx.monitor.stopProbes)

#### [module pmx.network](#apidoc.module.pmx.network)
1.  [function <span class="apidocSignatureSpan">pmx.network.</span>catchPorts ()](#apidoc.element.pmx.network.catchPorts)
1.  [function <span class="apidocSignatureSpan">pmx.network.</span>catchTraffic ()](#apidoc.element.pmx.network.catchTraffic)

#### [module pmx.notify](#apidoc.module.pmx.notify)
1.  [function <span class="apidocSignatureSpan">pmx.</span>notify (err)](#apidoc.element.pmx.notify.notify)
1.  [function <span class="apidocSignatureSpan">pmx.notify.</span>_interpretError (err)](#apidoc.element.pmx.notify._interpretError)
1.  [function <span class="apidocSignatureSpan">pmx.notify.</span>catchAll (opts)](#apidoc.element.pmx.notify.catchAll)
1.  [function <span class="apidocSignatureSpan">pmx.notify.</span>expressErrorHandler ()](#apidoc.element.pmx.notify.expressErrorHandler)

#### [module pmx.transaction](#apidoc.module.pmx.transaction)
1.  [function <span class="apidocSignatureSpan">pmx.transaction.</span>http (opts)](#apidoc.element.pmx.transaction.http)
1.  [function <span class="apidocSignatureSpan">pmx.transaction.</span>tracing (pmx, opts)](#apidoc.element.pmx.transaction.tracing)



# <a name="apidoc.module.pmx"></a>[module pmx](#apidoc.module.pmx)

#### <a name="apidoc.element.pmx._interpretError"></a>[function <span class="apidocSignatureSpan">pmx.</span>_interpretError (err)](#apidoc.element.pmx._interpretError)
- description and source-code
```javascript
_interpretError = function (err) {
  var s_err = {};

  if (typeof(err) === 'string') {
    // Simple string processing
    s_err.message = err;
    s_err.stack = err;
  }
  else if (!(err instanceof Error) && typeof(err) === 'object') {
    // JSON processing
    s_err.message = err;
    s_err.stack = err;
  }
  else if (err instanceof Error) {
    // Error object type processing
    err.stack;
    if (err.__error_callsites) {
      var stackFrames = [];
       err.__error_callsites.forEach(function(callSite) {
        stackFrames.push({ file_name: callSite.getFileName(), line_number: callSite.getLineNumber()});
      });
      err.stackframes = stackFrames;
      delete err.__error_callsites;
    }
    s_err = err;
  }

  return jsonize(s_err);
}
```
- example usage
```shell
...

if (listener === 'unhandledRejection') {
  error = 'You have triggered an unhandledRejection, you may have forgotten to catch a Promise rejection:\n' + error;
}

console.error(error);
if (err)
  var errObj = Notify._interpretError(err);

Transport.send({
  type : 'process:exception',
  data : errObj !== undefined ? errObj : {message: 'No error but ' + listener + ' was caught!' }
}, true);

if (!process.listeners(listener).filter(function (listener) {
...
```

#### <a name="apidoc.element.pmx.action"></a>[function <span class="apidocSignatureSpan">pmx.</span>action (action_name, opts, fn)](#apidoc.element.pmx.action)
- description and source-code
```javascript
action = function (action_name, opts, fn) {
  if (!fn) {
    fn = opts;
    opts = null;
  }

  if (!action_name)
    return console.error('[PMX] action.action_name is missing');
  if (!fn)
    return console.error('[PMX] emit.data is mission');

  if (!process.send) {
    debug('Process not running within PM2');
    return false;
  }

  // Notify the action
  Transport.send({
    type : 'axm:action',
    data : {
      action_name : action_name,
      opts        : opts,
      arity       : fn.length
    }
  });

  function reply(data) {
    if (data.length) {
      data._length = data.length;
      delete data.length;
    }

    Transport.send({
      type        : 'axm:reply',
      data        : {
        return      : data,
        action_name : action_name
      }
    });
  }

  process.on('message', function(data) {
    if (!data) return false;

    // In case 2 arguments has been set but no options has been transmitted
    if (fn.length === 2 && typeof(data) === 'string' && data === action_name)
      return fn({}, reply);

    // In case 1 arguments has been set but options has been transmitted
    if (fn.length === 1 && typeof(data) === 'object' && data.msg === action_name)
      return fn(reply);

<span class="apidocCodeCommentSpan">    /**
     * Classical call
     */
</span>    if (typeof(data) === 'string' && data === action_name)
      return fn(reply);

    /**
     * If data is an object == v2 protocol
     * Pass the opts as first argument
     */
    if (typeof(data) === 'object' && data.msg === action_name)
      return fn(data.opts, reply);
  });
}
```
- example usage
```shell
...
Simple action allows to trigger a function from Keymetrics. The function takes a function as a parameter (reply here) and need to
 be called once the job is finished.

Example:

'''javascript
var pmx = require('pmx');

pmx.action('db:clean', function(reply) {
  clean.db(function() {
    /**
     * reply() must be called at the end of the action
     */
     reply({success : true});
  });
});
...
```

#### <a name="apidoc.element.pmx.catchAll"></a>[function <span class="apidocSignatureSpan">pmx.</span>catchAll (opts)](#apidoc.element.pmx.catchAll)
- description and source-code
```javascript
catchAll = function (opts) {

  var callsites = require('./utils/error-callsites')

  if (opts === undefined)
    opts = { errors : true };

  Options.configureModule({
    error : opts.errors
  });

  if (process.env.exec_mode === 'cluster_mode')
    return false;

  function getUncaughtExceptionListener(listener) {
    return function uncaughtListener(err) {
      var error = err && err.stack ? err.stack : err;

      if (err && err.length) {
        err._length = err.length;
        delete err.length;
      }

      if (listener === 'unhandledRejection') {
        error = 'You have triggered an unhandledRejection, you may have forgotten to catch a Promise rejection:\n' + error;
      }

      console.error(error);
      if (err)
        var errObj = Notify._interpretError(err);

      Transport.send({
        type : 'process:exception',
        data : errObj !== undefined ? errObj : {message: 'No error but ' + listener + ' was caught!' }
      }, true);

      if (!process.listeners(listener).filter(function (listener) {
        return listener !== uncaughtListener;
      }).length) {

        if (listener == 'uncaughtException')
          process.exit(1);
      }
    }
  }

  if (opts.errors === true && util.inspect(process.listeners('uncaughtException')).length === 2) {
    process.once('uncaughtException', getUncaughtExceptionListener('uncaughtException'));
    process.once('unhandledRejection', getUncaughtExceptionListener('unhandledRejection'));
  }
  else if (opts.errors === false
           && util.inspect(process.listeners('uncaughtException')).length !== 2) {
    process.removeAllListeners('uncaughtException');
    process.removeAllListeners('unhandledRejection');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.catchPorts"></a>[function <span class="apidocSignatureSpan">pmx.</span>catchPorts ()](#apidoc.element.pmx.catchPorts)
- description and source-code
```javascript
catchPorts = function () {
  var ports_list = [];
  var opened_ports = 'N/A';

  Probe.probe().metric({
    name    : 'Open ports',
    value   : function() { return opened_ports; }
  });

  var original_listen = net_module.Server.prototype.listen;

  net_module.Server.prototype.listen = function() {
    var port = parseInt(arguments[0]);

    if (!isNaN(port) && ports_list.indexOf(port) === -1) {
      ports_list.push(port);
      opened_ports = ports_list.sort().join();
    }

    this.once('close', function() {
      if (ports_list.indexOf(port) > -1) {
        ports_list.splice(ports_list.indexOf(port), 1);
        opened_ports = ports_list.sort().join();
      }
    });

    return original_listen.apply(this, arguments);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.catchTraffic"></a>[function <span class="apidocSignatureSpan">pmx.</span>catchTraffic ()](#apidoc.element.pmx.catchTraffic)
- description and source-code
```javascript
catchTraffic = function () {
  var download = 0;
  var upload   = 0;
  var up       = '0 B/sec';
  var down     = '0 B/sec';

  var filter = function(bytes) {
    var to_fixed = 0;

    if (bytes === 0)
      ;
    else if (bytes < 1024)
      to_fixed = 6;
    else if (bytes < (1024 * 1024))
      to_fixed = 3;
    else
      to_fixed = 2;

    bytes = (bytes / (1024 * 1024)).toFixed(to_fixed);

    var cut_zeros = 0;

    for (var i = (bytes.length - 1); i > 0; --i) {
      if (bytes[i] === '.') {
        ++cut_zeros;
        break;
      }
      if (bytes[i] !== '0')
        break;
      ++cut_zeros;
    }

    if (cut_zeros > 0)
      bytes = bytes.slice(0, -(cut_zeros));

    return (bytes + ' MB/s');
  };

  var interval = setInterval(function() {
    up = filter(upload);
    down = filter(download);
    upload = 0;
    download = 0;
  }, 999);

  interval.unref();

  Probe.probe().metric({
    name     : 'Network Download',
    agg_type : 'sum',
    value    : function() { return down; }
  });

  Probe.probe().metric({
    name     : 'Network Upload',
    agg_type : 'sum',
    value    : function() { return up; }
  });

  var original_write = net_module.Socket.prototype.write;

  net_module.Socket.prototype.write = function(data) {
    if (data.length)
      upload += data.length;
    return original_write.apply(this, arguments);
  };

  var original_read = net_module.Socket.prototype.read;

  net_module.Socket.prototype.read = function() {

    if (!this.monitored) {
      this.monitored = true;

      this.on('data', function(data) {
        if (data.length)
          download += data.length;
      });
    }

    return original_read.apply(this, arguments);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.configureModule"></a>[function <span class="apidocSignatureSpan">pmx.</span>configureModule (opts)](#apidoc.element.pmx.configureModule)
- description and source-code
```javascript
configureModule = function (opts) {
  Transport.send({
    type : 'axm:option:configuration',
    data : opts
  }, false);
}
```
- example usage
```shell
...
} catch(e) {
  //console.error(e);
  //console.error('Error while parsing configuration in environment (%s)', conf.module_name);
}

if (do_not_tell_pm2 == true) return conf;

Options.configureModule(conf);
return conf;
};

Options.getPID = function(file) {
if (typeof(file) === 'number')
  return file;
return parseInt(fs.readFileSync(file).toString());
...
```

#### <a name="apidoc.element.pmx.detectV8Profiler"></a>[function <span class="apidocSignatureSpan">pmx.</span>detectV8Profiler (cb)](#apidoc.element.pmx.detectV8Profiler)
- description and source-code
```javascript
detectV8Profiler = function (cb) {
  var require_paths = require.main.paths.slice();

  (function look_for_profiler(require_paths) {
    if (!require_paths[0])
      return cb(new Error('Module not found'));

    var profiler_path = path.join(require_paths[0], 'v8-profiler');

    fs.exists(profiler_path, function(exist) {
      if (exist)
        return cb(null, profiler_path);

      require_paths.shift();
      return look_for_profiler(require_paths);
    });
    return false;
  })(require_paths);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.emit"></a>[function <span class="apidocSignatureSpan">pmx.</span>emit (name, data)](#apidoc.element.pmx.emit)
- description and source-code
```javascript
emit = function (name, data) {
  if (!name)
    return console.error('[AXM] emit.name is missing');
  if (!data)
    return console.error('[AXM] emit.data is missing');

  var inflight_obj = {};

  if (typeof(data) == 'object')
    inflight_obj = JSON.parse(stringify(data));
  else {
    inflight_obj.data = data;
  }

  inflight_obj.__name = name;

  Transport.send({
    type : 'human:event',
    data : inflight_obj
  }, true);
  return false;
}
```
- example usage
```shell
...

Emit events and get historical and statistics.
This is available in the **Events** page of Keymetrics.

'''javascript
var pmx = require('pmx');

pmx.emit('user:register', {
  user : 'Alex registered',
  email : 'thorustor@gmail.com'
});
'''

## Application level network traffic monitoring / Display used ports
...
```

#### <a name="apidoc.element.pmx.enableProbe"></a>[function <span class="apidocSignatureSpan">pmx.</span>enableProbe (custom_namespace)](#apidoc.element.pmx.enableProbe)
- description and source-code
```javascript
function enableProbes(custom_namespace) {
  if (!custom_namespace)
    custom_namespace = 'axm';

  if (!global[custom_namespace])
    global[custom_namespace] = {};

  if (this.interval)
    return global[custom_namespace];

  this.interval = setInterval(function() {
    Transport.send({
      type : 'axm:monitor',
      data : cookData(global[custom_namespace])
    });
  }, 990);

  this.interval.unref();

  return global[custom_namespace];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.enableProbes"></a>[function <span class="apidocSignatureSpan">pmx.</span>enableProbes (custom_namespace)](#apidoc.element.pmx.enableProbes)
- description and source-code
```javascript
function enableProbes(custom_namespace) {
  if (!custom_namespace)
    custom_namespace = 'axm';

  if (!global[custom_namespace])
    global[custom_namespace] = {};

  if (this.interval)
    return global[custom_namespace];

  this.interval = setInterval(function() {
    Transport.send({
      type : 'axm:monitor',
      data : cookData(global[custom_namespace])
    });
  }, 990);

  this.interval.unref();

  return global[custom_namespace];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.exposeProfiling"></a>[function <span class="apidocSignatureSpan">pmx.</span>exposeProfiling (pmx, profiler_path)](#apidoc.element.pmx.exposeProfiling)
- description and source-code
```javascript
exposeProfiling = function (pmx, profiler_path) {
  try {
    var profiler = require(profiler_path);
  } catch(e) {
    debug('v8-profiler module not installed', e);
    return false;
  }

  debug('v8-profiler sucessfully enabled');

<span class="apidocCodeCommentSpan">  /**
   * Tell Keymetrics that profiling is possible
   * (flag available in axm_options object)
   */
</span>  Options.configureModule({
    heapdump : true
  });

  /**
   * Heap snapshot
   */
  pmx.action('km:heapdump', function(reply) {
    var dump_file = path.join(os.tmpDir(), Date.now() + '.heapsnapshot');

    var snapshot = profiler.takeSnapshot('km-heap-snapshot');
    var buffer    = '';

    snapshot.serialize(
      function iterator(data, length) {
        buffer += data;
      }, function complete() {
        snapshot.delete();

        fs.writeFile(dump_file, buffer, function (err) {
          debug('Heap dump file flushed (e=', err);

          if (err) {
            return reply({
              success   : false,
              err : err
            });
          }
          return reply({
            success   : true,
            heapdump  : true,
            dump_file : dump_file
          });
        });
      }
    );
  });

  /**
   * CPU profiling snapshot
   */
  var ns_cpu_profiling        = 'km-cpu-profiling';
  var cpu_dump_file = path.join(os.tmpDir(), Date.now() + '.cpuprofile');

  pmx.action('km:cpu:profiling:start', function(reply) {
    profiler.startProfiling(ns_cpu_profiling);
    return reply({ success : true });
  });

  pmx.action('km:cpu:profiling:stop', function(reply) {
    var cpu = profiler.stopProfiling(ns_cpu_profiling);

    fs.writeFile(cpu_dump_file, JSON.stringify(cpu), function(err) {
      if (err) {
        return reply({
          success   : false,
          err : err
        });
      }
      return reply({
        success     : true,
        cpuprofile  : true,
        dump_file   : cpu_dump_file
      });
    });
  });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.expressErrorHandler"></a>[function <span class="apidocSignatureSpan">pmx.</span>expressErrorHandler ()](#apidoc.element.pmx.expressErrorHandler)
- description and source-code
```javascript
expressErrorHandler = function () {
  var self = this;

  Options.configureModule({
    error : true
  });

  return function errorHandler(err, req, res, next) {
    if (res.statusCode < 400) res.statusCode = 500;

    //debug(err.stack || err);

    err.url = req.url;
    err.component = req.url;
    err.action = req.method;
    err.params = req.body;
    err.session = req.session;

    Transport.send({
      type  : 'process:exception',
      data  : jsonize(err)
    }, true);
    return next(err);
  };
}
```
- example usage
```shell
...

// All my routes
app.get('/' ...);
app.post(...);
// All my routes

// Here I attach the middleware to get more verbosity on exception thrown
app.use(pmx.expressErrorHandler());
'''

## Emit Events

Emit events and get historical and statistics.
This is available in the **Events** page of Keymetrics.
...
```

#### <a name="apidoc.element.pmx.getConf"></a>[function <span class="apidocSignatureSpan">pmx.</span>getConf ()](#apidoc.element.pmx.getConf)
- description and source-code
```javascript
getConf = function () {
  return this._pmx_conf;
}
```
- example usage
```shell
...
  Probe._var[opts.name].alert = new Alert(alert_opts, {name : opts.name});
}
}

Probe.probe = function() {
var self = this;
// Get module configuration to enable alerts
if (this.getConf && this.getConf())
  Probe._alert_activated = this.getConf().alert_enabled || true;
else
  Probe._alert_activated = false;

if (Probe._started == false) {
  Probe._started = true;
...
```

#### <a name="apidoc.element.pmx.getEnv"></a>[function <span class="apidocSignatureSpan">pmx.</span>getEnv ()](#apidoc.element.pmx.getEnv)
- description and source-code
```javascript
getEnv = function () {
  return process.env;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.getPID"></a>[function <span class="apidocSignatureSpan">pmx.</span>getPID (file)](#apidoc.element.pmx.getPID)
- description and source-code
```javascript
getPID = function (file) {
  if (typeof(file) === 'number')
    return file;
  return parseInt(fs.readFileSync(file).toString());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.http"></a>[function <span class="apidocSignatureSpan">pmx.</span>http (opts)](#apidoc.element.pmx.http)
- description and source-code
```javascript
http = function (opts) {
  var Module = require('module');

  debug('Wrapping HTTP routes');

  if (Array.isArray(opts)) {
    var routes = JSON.parse(JSON.stringify(opts));
    opts = {
      http          : true,
      http_latency  : 200,
      http_code     : 500,
      ignore_routes : routes
    };
  }
  opts = util._extend({
    http          : true,
    http_latency  : 200,
    http_code     : 500,
    ignore_routes : []
  }, opts);

  Proxy.wrap(Module, '_load', function(load) {
    if (load.__axm_original) {
      debug('HTTP routes have already been wrapped before');

      Options.configureModule({
        latency : opts.http
      });

      if (opts.http === false) {
        return function(file) { return load.__axm_original.apply(this, arguments) };
      } else {
        return function(file) {
          if (file === 'http' || file === 'https')
            return SimpleHttpWrap(opts, load.__axm_original.apply(this, arguments));
          else
            return load.__axm_original.apply(this, arguments);
        };
      }
    }

    return function(file) {
      if (opts.http &&
          (file === 'http' || file === 'https')) {
        debug('http module being required');
        Options.configureModule({
          latency : true
        });
        return SimpleHttpWrap(opts, load.apply(this, arguments));
      }
      else
        return load.apply(this, arguments);
    };
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.init"></a>[function <span class="apidocSignatureSpan">pmx.</span>init (opts)](#apidoc.element.pmx.init)
- description and source-code
```javascript
init = function (opts) {
  if (!opts) opts = {};

  opts = util._extend({
    default_actions : true,
    transactions  : false,
    http          : true,
    http_latency  : 200,
    http_code     : 500,
    ignore_routes : [],
    profiling     : true,
    errors        : true,
    // By default if you add alert subfield in custom
    // it's going to be enabled
    alert_enabled : true,
    custom_probes : true,
    network       : false,
    ports         : false,

    // VXX options
    // ignoreFilter.url is aliased to ignore_routes
    ignoreFilter: {
      'url': [],
      'method': ['OPTIONS']
    },
    // 'express', 'hapi', 'http', 'restify'
    excludedHooks: []
  }, opts);

  opts = Configuration.init(opts);
  this._pmx_conf = opts;

  if (opts.ports)
    PMX.catchPorts();
  if (opts.network)
    PMX.catchTraffic();

  if (opts.transactions)
    PMX.tracing(PMX, opts);
  if (opts.http)
    PMX.http(opts);

  PMX.catchAll(opts);

  if (opts.profiling)
    Profiling.v8Profiling(PMX);

  if (opts.custom_probes == true) {
    // Event loop monitoring
    require('./probes/pacemaker.js')(PMX);
  }

  if (opts.default_actions == true) {
    //require('./actions/default.js')(PMX);
  }

  opts.isModule = false;
  return this;
}
```
- example usage
```shell
...
You can monitor the network usage of a specific application by adding the option 'network: true' when initializing PMX. If you enable
 the flag 'ports: true' when you init pmx it will show which ports your app is listenting on.

These metrics will be shown in the Keymetrics Dashboard in the Custom Metrics section.

Example:

'''javascript
pmx.init({
  [...]
  network : true, // Allow application level network monitoring
  ports   : true  // Display ports used by the application
});
'''

## Advanced PMX configuration
...
```

#### <a name="apidoc.element.pmx.initModule"></a>[function <span class="apidocSignatureSpan">pmx.</span>initModule (opts, cb)](#apidoc.element.pmx.initModule)
- description and source-code
```javascript
initModule = function (opts, cb) {
  if (!opts) opts = {};

  opts = util._extend({
    alert_enabled    : true,
    widget           : {}
  }, opts);

  opts.widget = util._extend({
    type : 'generic',
    logo : 'https://app.keymetrics.io/img/logo/keymetrics-300.png',
    theme            : ['#111111', '#1B2228', '#807C7C', '#807C7C']
  }, opts.widget);

  opts.isModule = true;
  opts = Configuration.init(opts);

  // Force error catching
  PMX.catchAll();

  this._pmx_conf = opts;

  if (cb && typeof(cb) == 'function')
    return cb(null, opts);

  return opts;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.notify"></a>[function <span class="apidocSignatureSpan">pmx.</span>notify (err)](#apidoc.element.pmx.notify)
- description and source-code
```javascript
notify = function (err) {
  var ret_err = this._interpretError(err);

  // full_err
  //debug(ret_err);

  Transport.send({
    type : 'process:exception',
    data : ret_err
  }, true);

  return ret_err;
}
```
- example usage
```shell
...
### Custom alert notification

If you need to alert about any critical errors you can do it programmatically:

'''javascript
var pmx = require('pmx');

pmx.notify({ success : false });

pmx.notify('This is an error');

pmx.notify(new Error('This is an error'));
'''

### Add Verbosity to an Alert: Express Error handler
...
```

#### <a name="apidoc.element.pmx.probe"></a>[function <span class="apidocSignatureSpan">pmx.</span>probe ()](#apidoc.element.pmx.probe)
- description and source-code
```javascript
probe = function () {
  var self = this;
  // Get module configuration to enable alerts
  if (this.getConf && this.getConf())
    Probe._alert_activated = this.getConf().alert_enabled || true;
  else
    Probe._alert_activated = false;

  if (Probe._started == false) {
    Probe._started = true;

    var p_interval = setInterval(function() {
      Transport.send({
        type : 'axm:monitor',
        data : cookData(Probe._var)
      });
      checkIssues(Probe._var);
    }, 990);

    p_interval.unref();
  }

  return {
<span class="apidocCodeCommentSpan">    /**
     * This reflect data to keymetrics
     * pmx.transpose('prop name', fn)
     *
     * or
     *
     * pmx.transpose({
     *   name : 'variable name',
     *   data : function() { return value }
     * });
     */
</span>    transpose : function(variable_name, reporter) {
      if (typeof variable_name === 'object') {
        reporter = variable_name.data;
        variable_name = variable_name.name;
      }

      if (typeof reporter !== 'function') {
        return console.error('[PMX] reporter is not a function');
      }

      Probe._var[variable_name] = {
        value: reporter
      };
    },
    metric : function(opts) {
      var agg_type = opts.agg_type || Probe.default_aggregation;

      if (!opts.name)
        return console.error('[Probe][Metric] Name not defined');
      if (Probe.AVAILABLE_AGG_TYPES.indexOf(agg_type) == -1)
        return console.error("[Probe][Metric] Unknown agg_type: %s", agg_type);

      Probe._var[opts.name] = {
        value   : opts.value || 0,
        agg_type: agg_type
      };

      /**
       * Attach alert to: Probe._var[opts.name].alert
       */
      if (self.getConf)
        attachAlert(opts, self.getConf());

      return {
        val : function() {
          var value = Probe._var[opts.name].value;

          if (typeof(value) == 'function')
            value = value();

          return value;
        },
        set : function(dt) {
          Probe._var[opts.name].value = dt;
        }
      };
    },
    histogram : function(opts) {
      if (!opts.name)
        return console.error('[Probe][Histogram] Name not defined');
      opts.measurement = opts.measurement || 'mean';
      opts.unit = opts.unit || '';
      var agg_type = opts.agg_type || Probe.default_aggregation;

      if (Probe.AVAILABLE_MEASUREMENTS.indexOf(opts.measurement) == -1)
        return console.error('[Probe][Histogram] Measure type %s does not exists', opts.measurement);
      if (Probe.AVAILABLE_AGG_TYPES.indexOf(agg_type) == -1)
        return console.error("[Probe][Metric] Unknown agg_type: %s", agg_type);

      var histogram = new Histogram(opts);

      Probe._var[opts.name] = {
        value: function() { return (Math.round(histogram.val() * 100) / 100) + '' + opts.unit },
        agg_type: agg_type
      };

      /**
       * Attach alert to: Probe._var[opts.name].alert
       */
      if (self.getConf)
        attachAlert(opts, self.getConf());

      return histogram;
    },
    meter : function(opts) {
      var agg_type = opts.agg_type || Probe.default_aggregation;

      if (!opts.name)
        return console.error('[Probe][Meter] Name not defined');
      if (Probe.AVAILABLE_AGG_TYPES.indexOf(agg_type) == -1)
        return console.error("[Probe][Metric] Unknown agg_type: %s", agg_type);

      opts.unit = opts.unit || '';

      var meter = new Meter(opts);

      Probe._var[opts.name] = {
        value: function() { return meter.val() + '' + opts.unit },
        agg_type: agg_type
      };

      /**
       * Attach alert to: Probe._var[opts.name].alert
       */
      if (self.getConf)
        attachAlert(opts, self.getConf());

      return meter;
    },
    counter : function(opts) {
      var agg_type = opts.agg_type || Probe.default_aggregation;

      if (!opts.name)
        return console.error('[Probe][Counter] Name not defined');
      if (Probe.AVAILABLE_AGG_TYPES.indexOf(agg_type) == -1)
        return console.error("[Probe][Metric] Unknown agg_type: %s", agg_type);

      var counter = new Counter();

      Probe._var[opts.name] = {
        value: ...
```
- example usage
```shell
...
  - eg. Monitor the mean of execution of a query into database

### Metric: Simple value reporting

This allow to expose values that can be read instantly.

'''javascript
var probe = pmx.probe();

// Here the value function will be called each second to get the value
// returned by Object.keys(users).length
var metric = probe.metric({
name    : 'Realtime user',
value   : function() {
  return Object.keys(users).length;
...
```

#### <a name="apidoc.element.pmx.resolvePidPaths"></a>[function <span class="apidocSignatureSpan">pmx.</span>resolvePidPaths (filepaths)](#apidoc.element.pmx.resolvePidPaths)
- description and source-code
```javascript
resolvePidPaths = function (filepaths) {
  if (typeof(filepaths) === 'number')
    return filepaths;

  function detect(filepaths) {
    var content = '';

    filepaths.some(function(filepath) {
      try {
        content = fs.readFileSync(filepath);
      } catch(e) {
        return false;
      }
      return true;
    });

    return content.toString().trim();
  }

  var ret = parseInt(detect(filepaths));

  return isNaN(ret) ? null : ret;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.scopedAction"></a>[function <span class="apidocSignatureSpan">pmx.</span>scopedAction (action_name, fn)](#apidoc.element.pmx.scopedAction)
- description and source-code
```javascript
scopedAction = function (action_name, fn) {

  if (!action_name)
    return console.error('[PMX] action.action_name is missing');
  if (!fn)
    return console.error('[PMX] callback is missing');

  if (!process.send) {
    debug('Process not running within PM2');
    return false;
  }

  // Notify the action
  Transport.send({
    type : 'axm:action',
    data : {
      action_name : action_name,
      action_type : 'scoped'
    }
  });

  process.on('message', function(data) {
    if (!data
        || data.uuid === undefined
        || data.action_name === undefined)
      return false;

    if (data.action_name === action_name) {
      var res = {
        send : function(dt) {
          Transport.send({
            type        : 'axm:scoped_action:stream',
            data        : {
              data        : dt,
              uuid        : data.uuid,
              action_name : action_name
            }
          });
        },
        error : function(dt) {
          Transport.send({
            type        : 'axm:scoped_action:error',
            data        : {
              data        : dt,
              uuid        : data.uuid,
              action_name : action_name
            }
          });
        },
        end : function(dt) {
          Transport.send({
            type        : 'axm:scoped_action:end',
            data        : {
              data        : dt,
              uuid        : data.uuid,
              action_name : action_name
            }
          });
        }
      };

      var d = domain.create();

      d.on('error', function(err) {
        res.error(err.message || err.stack || err);
        setTimeout(function() {
          process.exit(1);
        }, 300);
      });

      d.run(function() {
        fn(data.opts || null, res);
      });
    }
  });
}
```
- example usage
```shell
...
Scoped Actions are advanced remote actions that can be also triggered from Keymetrics.

Two arguments are passed to the function, data (optional data sent from Keymetrics) and res that allows to emit log data and to
end the scoped action.

Example:

'''javascript
pmx.scopedAction('long running lsof', function(data, res) {
var child = spawn('lsof', []);

child.stdout.on('data', function(chunk) {
  chunk.toString().split('\n').forEach(function(line) {
    res.send(line); // This send log to Keymetrics to be saved (for tracking)
  });
});
...
```

#### <a name="apidoc.element.pmx.stopProbe"></a>[function <span class="apidocSignatureSpan">pmx.</span>stopProbe ()](#apidoc.element.pmx.stopProbe)
- description and source-code
```javascript
function stopProbing() {
  clearInterval(this.interval);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.stopProbes"></a>[function <span class="apidocSignatureSpan">pmx.</span>stopProbes ()](#apidoc.element.pmx.stopProbes)
- description and source-code
```javascript
function stopProbing() {
  clearInterval(this.interval);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.tracing"></a>[function <span class="apidocSignatureSpan">pmx.</span>tracing (pmx, opts)](#apidoc.element.pmx.tracing)
- description and source-code
```javascript
tracing = function (pmx, opts) {

  if (Array.isArray(opts.ignore_routes) && opts.ignore_routes.length > 0) {
    opts.ignoreFilter.url = opts.ignore_routes;
  }

  Transaction.tracer = require('vxx').start(opts);

  Options.configureModule({
    tracing_enabled : true
  });

  // broadcast to pm2 aggregator
  Transaction.tracer.getBus().on('transaction', function(data) {
    Transport.send({
      type: 'axm:trace',
      data: data
    })
  })

  // Transaction.tracer.getBus().on('transaction', function (data) {
  //   if (!opts.custom_probes) return;
  //   // TODO: mine tracing data and require custom probes
  //<span class="apidocCodeCommentSpan">   /*try {
  //     var custom_probe = require('./probes/' + modul)(pmx, Transaction.tracer)
  //   } catch (err) { }*/
</span>  // })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.v8Profiling"></a>[function <span class="apidocSignatureSpan">pmx.</span>v8Profiling (pmx)](#apidoc.element.pmx.v8Profiling)
- description and source-code
```javascript
v8Profiling = function (pmx) {
  Profiling.detectV8Profiler(function(err, profiler_path) {
    if (err)
      return false;
    return Profiling.exposeProfiling(pmx, profiler_path);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pmx.Probe"></a>[module pmx.Probe](#apidoc.module.pmx.Probe)

#### <a name="apidoc.element.pmx.Probe.probe"></a>[function <span class="apidocSignatureSpan">pmx.Probe.</span>probe ()](#apidoc.element.pmx.Probe.probe)
- description and source-code
```javascript
probe = function () {
  var self = this;
  // Get module configuration to enable alerts
  if (this.getConf && this.getConf())
    Probe._alert_activated = this.getConf().alert_enabled || true;
  else
    Probe._alert_activated = false;

  if (Probe._started == false) {
    Probe._started = true;

    var p_interval = setInterval(function() {
      Transport.send({
        type : 'axm:monitor',
        data : cookData(Probe._var)
      });
      checkIssues(Probe._var);
    }, 990);

    p_interval.unref();
  }

  return {
<span class="apidocCodeCommentSpan">    /**
     * This reflect data to keymetrics
     * pmx.transpose('prop name', fn)
     *
     * or
     *
     * pmx.transpose({
     *   name : 'variable name',
     *   data : function() { return value }
     * });
     */
</span>    transpose : function(variable_name, reporter) {
      if (typeof variable_name === 'object') {
        reporter = variable_name.data;
        variable_name = variable_name.name;
      }

      if (typeof reporter !== 'function') {
        return console.error('[PMX] reporter is not a function');
      }

      Probe._var[variable_name] = {
        value: reporter
      };
    },
    metric : function(opts) {
      var agg_type = opts.agg_type || Probe.default_aggregation;

      if (!opts.name)
        return console.error('[Probe][Metric] Name not defined');
      if (Probe.AVAILABLE_AGG_TYPES.indexOf(agg_type) == -1)
        return console.error("[Probe][Metric] Unknown agg_type: %s", agg_type);

      Probe._var[opts.name] = {
        value   : opts.value || 0,
        agg_type: agg_type
      };

      /**
       * Attach alert to: Probe._var[opts.name].alert
       */
      if (self.getConf)
        attachAlert(opts, self.getConf());

      return {
        val : function() {
          var value = Probe._var[opts.name].value;

          if (typeof(value) == 'function')
            value = value();

          return value;
        },
        set : function(dt) {
          Probe._var[opts.name].value = dt;
        }
      };
    },
    histogram : function(opts) {
      if (!opts.name)
        return console.error('[Probe][Histogram] Name not defined');
      opts.measurement = opts.measurement || 'mean';
      opts.unit = opts.unit || '';
      var agg_type = opts.agg_type || Probe.default_aggregation;

      if (Probe.AVAILABLE_MEASUREMENTS.indexOf(opts.measurement) == -1)
        return console.error('[Probe][Histogram] Measure type %s does not exists', opts.measurement);
      if (Probe.AVAILABLE_AGG_TYPES.indexOf(agg_type) == -1)
        return console.error("[Probe][Metric] Unknown agg_type: %s", agg_type);

      var histogram = new Histogram(opts);

      Probe._var[opts.name] = {
        value: function() { return (Math.round(histogram.val() * 100) / 100) + '' + opts.unit },
        agg_type: agg_type
      };

      /**
       * Attach alert to: Probe._var[opts.name].alert
       */
      if (self.getConf)
        attachAlert(opts, self.getConf());

      return histogram;
    },
    meter : function(opts) {
      var agg_type = opts.agg_type || Probe.default_aggregation;

      if (!opts.name)
        return console.error('[Probe][Meter] Name not defined');
      if (Probe.AVAILABLE_AGG_TYPES.indexOf(agg_type) == -1)
        return console.error("[Probe][Metric] Unknown agg_type: %s", agg_type);

      opts.unit = opts.unit || '';

      var meter = new Meter(opts);

      Probe._var[opts.name] = {
        value: function() { return meter.val() + '' + opts.unit },
        agg_type: agg_type
      };

      /**
       * Attach alert to: Probe._var[opts.name].alert
       */
      if (self.getConf)
        attachAlert(opts, self.getConf());

      return meter;
    },
    counter : function(opts) {
      var agg_type = opts.agg_type || Probe.default_aggregation;

      if (!opts.name)
        return console.error('[Probe][Counter] Name not defined');
      if (Probe.AVAILABLE_AGG_TYPES.indexOf(agg_type) == -1)
        return console.error("[Probe][Metric] Unknown agg_type: %s", agg_type);

      var counter = new Counter();

      Probe._var[opts.name] = {
        value: ...
```
- example usage
```shell
...
  - eg. Monitor the mean of execution of a query into database

### Metric: Simple value reporting

This allow to expose values that can be read instantly.

'''javascript
var probe = pmx.probe();

// Here the value function will be called each second to get the value
// returned by Object.keys(users).length
var metric = probe.metric({
name    : 'Realtime user',
value   : function() {
  return Object.keys(users).length;
...
```



# <a name="apidoc.module.pmx.actions"></a>[module pmx.actions](#apidoc.module.pmx.actions)

#### <a name="apidoc.element.pmx.actions.action"></a>[function <span class="apidocSignatureSpan">pmx.actions.</span>action (action_name, opts, fn)](#apidoc.element.pmx.actions.action)
- description and source-code
```javascript
action = function (action_name, opts, fn) {
  if (!fn) {
    fn = opts;
    opts = null;
  }

  if (!action_name)
    return console.error('[PMX] action.action_name is missing');
  if (!fn)
    return console.error('[PMX] emit.data is mission');

  if (!process.send) {
    debug('Process not running within PM2');
    return false;
  }

  // Notify the action
  Transport.send({
    type : 'axm:action',
    data : {
      action_name : action_name,
      opts        : opts,
      arity       : fn.length
    }
  });

  function reply(data) {
    if (data.length) {
      data._length = data.length;
      delete data.length;
    }

    Transport.send({
      type        : 'axm:reply',
      data        : {
        return      : data,
        action_name : action_name
      }
    });
  }

  process.on('message', function(data) {
    if (!data) return false;

    // In case 2 arguments has been set but no options has been transmitted
    if (fn.length === 2 && typeof(data) === 'string' && data === action_name)
      return fn({}, reply);

    // In case 1 arguments has been set but options has been transmitted
    if (fn.length === 1 && typeof(data) === 'object' && data.msg === action_name)
      return fn(reply);

<span class="apidocCodeCommentSpan">    /**
     * Classical call
     */
</span>    if (typeof(data) === 'string' && data === action_name)
      return fn(reply);

    /**
     * If data is an object == v2 protocol
     * Pass the opts as first argument
     */
    if (typeof(data) === 'object' && data.msg === action_name)
      return fn(data.opts, reply);
  });
}
```
- example usage
```shell
...
Simple action allows to trigger a function from Keymetrics. The function takes a function as a parameter (reply here) and need to
 be called once the job is finished.

Example:

'''javascript
var pmx = require('pmx');

pmx.action('db:clean', function(reply) {
  clean.db(function() {
    /**
     * reply() must be called at the end of the action
     */
     reply({success : true});
  });
});
...
```

#### <a name="apidoc.element.pmx.actions.scopedAction"></a>[function <span class="apidocSignatureSpan">pmx.actions.</span>scopedAction (action_name, fn)](#apidoc.element.pmx.actions.scopedAction)
- description and source-code
```javascript
scopedAction = function (action_name, fn) {

  if (!action_name)
    return console.error('[PMX] action.action_name is missing');
  if (!fn)
    return console.error('[PMX] callback is missing');

  if (!process.send) {
    debug('Process not running within PM2');
    return false;
  }

  // Notify the action
  Transport.send({
    type : 'axm:action',
    data : {
      action_name : action_name,
      action_type : 'scoped'
    }
  });

  process.on('message', function(data) {
    if (!data
        || data.uuid === undefined
        || data.action_name === undefined)
      return false;

    if (data.action_name === action_name) {
      var res = {
        send : function(dt) {
          Transport.send({
            type        : 'axm:scoped_action:stream',
            data        : {
              data        : dt,
              uuid        : data.uuid,
              action_name : action_name
            }
          });
        },
        error : function(dt) {
          Transport.send({
            type        : 'axm:scoped_action:error',
            data        : {
              data        : dt,
              uuid        : data.uuid,
              action_name : action_name
            }
          });
        },
        end : function(dt) {
          Transport.send({
            type        : 'axm:scoped_action:end',
            data        : {
              data        : dt,
              uuid        : data.uuid,
              action_name : action_name
            }
          });
        }
      };

      var d = domain.create();

      d.on('error', function(err) {
        res.error(err.message || err.stack || err);
        setTimeout(function() {
          process.exit(1);
        }, 300);
      });

      d.run(function() {
        fn(data.opts || null, res);
      });
    }
  });
}
```
- example usage
```shell
...
Scoped Actions are advanced remote actions that can be also triggered from Keymetrics.

Two arguments are passed to the function, data (optional data sent from Keymetrics) and res that allows to emit log data and to
end the scoped action.

Example:

'''javascript
pmx.scopedAction('long running lsof', function(data, res) {
var child = spawn('lsof', []);

child.stdout.on('data', function(chunk) {
  chunk.toString().split('\n').forEach(function(line) {
    res.send(line); // This send log to Keymetrics to be saved (for tracking)
  });
});
...
```



# <a name="apidoc.module.pmx.common"></a>[module pmx.common](#apidoc.module.pmx.common)

#### <a name="apidoc.element.pmx.common.getDate"></a>[function <span class="apidocSignatureSpan">pmx.common.</span>getDate ()](#apidoc.element.pmx.common.getDate)
- description and source-code
```javascript
function getDate() {
  return Math.round(Date.now() / 1000);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pmx.configuration"></a>[module pmx.configuration](#apidoc.module.pmx.configuration)

#### <a name="apidoc.element.pmx.configuration.configureModule"></a>[function <span class="apidocSignatureSpan">pmx.configuration.</span>configureModule (opts)](#apidoc.element.pmx.configuration.configureModule)
- description and source-code
```javascript
configureModule = function (opts) {
  Transport.send({
    type : 'axm:option:configuration',
    data : opts
  }, false);
}
```
- example usage
```shell
...
} catch(e) {
  //console.error(e);
  //console.error('Error while parsing configuration in environment (%s)', conf.module_name);
}

if (do_not_tell_pm2 == true) return conf;

Options.configureModule(conf);
return conf;
};

Options.getPID = function(file) {
if (typeof(file) === 'number')
  return file;
return parseInt(fs.readFileSync(file).toString());
...
```

#### <a name="apidoc.element.pmx.configuration.getPID"></a>[function <span class="apidocSignatureSpan">pmx.configuration.</span>getPID (file)](#apidoc.element.pmx.configuration.getPID)
- description and source-code
```javascript
getPID = function (file) {
  if (typeof(file) === 'number')
    return file;
  return parseInt(fs.readFileSync(file).toString());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.configuration.init"></a>[function <span class="apidocSignatureSpan">pmx.configuration.</span>init (conf, do_not_tell_pm2)](#apidoc.element.pmx.configuration.init)
- description and source-code
```javascript
init = function (conf, do_not_tell_pm2) {
  var package_filepath = findPackageJson();
  var package_json;

  if (!conf.module_conf)
    conf.module_conf = {};

  if (conf.isModule == true) {
<span class="apidocCodeCommentSpan">    /**
     * Merge package.json metadata
     */
</span>    try {
      package_json = require(package_filepath);

      conf.module_version = package_json.version;
      conf.module_name    = package_json.name;
      conf.description    = package_json.description;
      conf.pmx_version    = null;

      if (pkg.version)
        conf.pmx_version    = pkg.version;

      if (package_json.config) {
        conf = util._extend(conf, package_json.config);
        conf.module_conf = package_json.config;
      }
    } catch(e) {
      throw new Error(e);
    }
  } else {
    conf.module_name = process.env.name || 'outside-pm2';
    try {
      package_json = require(package_filepath);

      conf.module_version = package_json.version;
      conf.pmx_version    = null;

      if (pkg.version)
        conf.pmx_version    = pkg.version;

      if (package_json.config) {
        conf = util._extend(conf, package_json.config);
        conf.module_conf = package_json.config;
      }
    } catch(e) {
    }
  }

  /**
   * If custom variables has been set, merge with returned configuration
   */
  try {
    if (process.env[conf.module_name]) {
      var casted_conf = Autocast(JSON.parse(process.env[conf.module_name]));
      conf = util._extend(conf, casted_conf);
      // Do not display probe configuration in Keymetrics
      delete casted_conf.probes;
      // This is the configuration variable modifiable from keymetrics
      conf.module_conf = JSON.parse(JSON.stringify(util._extend(conf.module_conf, casted_conf)));

      // Obfuscate passwords
      Object.keys(conf.module_conf).forEach(function(key) {
        if ((key == 'password' || key == 'passwd') &&
            conf.module_conf[key].length >= 1) {
          conf.module_conf[key] = 'Password hidden';
        }

      });
    }
  } catch(e) {
    //console.error(e);
    //console.error('Error while parsing configuration in environment (%s)', conf.module_name);
  }

  if (do_not_tell_pm2 == true) return conf;

  Options.configureModule(conf);
  return conf;
}
```
- example usage
```shell
...
You can monitor the network usage of a specific application by adding the option 'network: true' when initializing PMX. If you enable
 the flag 'ports: true' when you init pmx it will show which ports your app is listenting on.

These metrics will be shown in the Keymetrics Dashboard in the Custom Metrics section.

Example:

'''javascript
pmx.init({
  [...]
  network : true, // Allow application level network monitoring
  ports   : true  // Display ports used by the application
});
'''

## Advanced PMX configuration
...
```

#### <a name="apidoc.element.pmx.configuration.resolvePidPaths"></a>[function <span class="apidocSignatureSpan">pmx.configuration.</span>resolvePidPaths (filepaths)](#apidoc.element.pmx.configuration.resolvePidPaths)
- description and source-code
```javascript
resolvePidPaths = function (filepaths) {
  if (typeof(filepaths) === 'number')
    return filepaths;

  function detect(filepaths) {
    var content = '';

    filepaths.some(function(filepath) {
      try {
        content = fs.readFileSync(filepath);
      } catch(e) {
        return false;
      }
      return true;
    });

    return content.toString().trim();
  }

  var ret = parseInt(detect(filepaths));

  return isNaN(ret) ? null : ret;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pmx.events"></a>[module pmx.events](#apidoc.module.pmx.events)

#### <a name="apidoc.element.pmx.events.emit"></a>[function <span class="apidocSignatureSpan">pmx.events.</span>emit (name, data)](#apidoc.element.pmx.events.emit)
- description and source-code
```javascript
emit = function (name, data) {
  if (!name)
    return console.error('[AXM] emit.name is missing');
  if (!data)
    return console.error('[AXM] emit.data is missing');

  var inflight_obj = {};

  if (typeof(data) == 'object')
    inflight_obj = JSON.parse(stringify(data));
  else {
    inflight_obj.data = data;
  }

  inflight_obj.__name = name;

  Transport.send({
    type : 'human:event',
    data : inflight_obj
  }, true);
  return false;
}
```
- example usage
```shell
...

Emit events and get historical and statistics.
This is available in the **Events** page of Keymetrics.

'''javascript
var pmx = require('pmx');

pmx.emit('user:register', {
  user : 'Alex registered',
  email : 'thorustor@gmail.com'
});
'''

## Application level network traffic monitoring / Display used ports
...
```



# <a name="apidoc.module.pmx.monitor"></a>[module pmx.monitor](#apidoc.module.pmx.monitor)

#### <a name="apidoc.element.pmx.monitor.enableProbe"></a>[function <span class="apidocSignatureSpan">pmx.monitor.</span>enableProbe (custom_namespace)](#apidoc.element.pmx.monitor.enableProbe)
- description and source-code
```javascript
function enableProbes(custom_namespace) {
  if (!custom_namespace)
    custom_namespace = 'axm';

  if (!global[custom_namespace])
    global[custom_namespace] = {};

  if (this.interval)
    return global[custom_namespace];

  this.interval = setInterval(function() {
    Transport.send({
      type : 'axm:monitor',
      data : cookData(global[custom_namespace])
    });
  }, 990);

  this.interval.unref();

  return global[custom_namespace];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.monitor.enableProbes"></a>[function <span class="apidocSignatureSpan">pmx.monitor.</span>enableProbes (custom_namespace)](#apidoc.element.pmx.monitor.enableProbes)
- description and source-code
```javascript
function enableProbes(custom_namespace) {
  if (!custom_namespace)
    custom_namespace = 'axm';

  if (!global[custom_namespace])
    global[custom_namespace] = {};

  if (this.interval)
    return global[custom_namespace];

  this.interval = setInterval(function() {
    Transport.send({
      type : 'axm:monitor',
      data : cookData(global[custom_namespace])
    });
  }, 990);

  this.interval.unref();

  return global[custom_namespace];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.monitor.stopProbe"></a>[function <span class="apidocSignatureSpan">pmx.monitor.</span>stopProbe ()](#apidoc.element.pmx.monitor.stopProbe)
- description and source-code
```javascript
function stopProbing() {
  clearInterval(this.interval);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.monitor.stopProbes"></a>[function <span class="apidocSignatureSpan">pmx.monitor.</span>stopProbes ()](#apidoc.element.pmx.monitor.stopProbes)
- description and source-code
```javascript
function stopProbing() {
  clearInterval(this.interval);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pmx.network"></a>[module pmx.network](#apidoc.module.pmx.network)

#### <a name="apidoc.element.pmx.network.catchPorts"></a>[function <span class="apidocSignatureSpan">pmx.network.</span>catchPorts ()](#apidoc.element.pmx.network.catchPorts)
- description and source-code
```javascript
catchPorts = function () {
  var ports_list = [];
  var opened_ports = 'N/A';

  Probe.probe().metric({
    name    : 'Open ports',
    value   : function() { return opened_ports; }
  });

  var original_listen = net_module.Server.prototype.listen;

  net_module.Server.prototype.listen = function() {
    var port = parseInt(arguments[0]);

    if (!isNaN(port) && ports_list.indexOf(port) === -1) {
      ports_list.push(port);
      opened_ports = ports_list.sort().join();
    }

    this.once('close', function() {
      if (ports_list.indexOf(port) > -1) {
        ports_list.splice(ports_list.indexOf(port), 1);
        opened_ports = ports_list.sort().join();
      }
    });

    return original_listen.apply(this, arguments);
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.network.catchTraffic"></a>[function <span class="apidocSignatureSpan">pmx.network.</span>catchTraffic ()](#apidoc.element.pmx.network.catchTraffic)
- description and source-code
```javascript
catchTraffic = function () {
  var download = 0;
  var upload   = 0;
  var up       = '0 B/sec';
  var down     = '0 B/sec';

  var filter = function(bytes) {
    var to_fixed = 0;

    if (bytes === 0)
      ;
    else if (bytes < 1024)
      to_fixed = 6;
    else if (bytes < (1024 * 1024))
      to_fixed = 3;
    else
      to_fixed = 2;

    bytes = (bytes / (1024 * 1024)).toFixed(to_fixed);

    var cut_zeros = 0;

    for (var i = (bytes.length - 1); i > 0; --i) {
      if (bytes[i] === '.') {
        ++cut_zeros;
        break;
      }
      if (bytes[i] !== '0')
        break;
      ++cut_zeros;
    }

    if (cut_zeros > 0)
      bytes = bytes.slice(0, -(cut_zeros));

    return (bytes + ' MB/s');
  };

  var interval = setInterval(function() {
    up = filter(upload);
    down = filter(download);
    upload = 0;
    download = 0;
  }, 999);

  interval.unref();

  Probe.probe().metric({
    name     : 'Network Download',
    agg_type : 'sum',
    value    : function() { return down; }
  });

  Probe.probe().metric({
    name     : 'Network Upload',
    agg_type : 'sum',
    value    : function() { return up; }
  });

  var original_write = net_module.Socket.prototype.write;

  net_module.Socket.prototype.write = function(data) {
    if (data.length)
      upload += data.length;
    return original_write.apply(this, arguments);
  };

  var original_read = net_module.Socket.prototype.read;

  net_module.Socket.prototype.read = function() {

    if (!this.monitored) {
      this.monitored = true;

      this.on('data', function(data) {
        if (data.length)
          download += data.length;
      });
    }

    return original_read.apply(this, arguments);
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pmx.notify"></a>[module pmx.notify](#apidoc.module.pmx.notify)

#### <a name="apidoc.element.pmx.notify.notify"></a>[function <span class="apidocSignatureSpan">pmx.</span>notify (err)](#apidoc.element.pmx.notify.notify)
- description and source-code
```javascript
notify = function (err) {
  var ret_err = this._interpretError(err);

  // full_err
  //debug(ret_err);

  Transport.send({
    type : 'process:exception',
    data : ret_err
  }, true);

  return ret_err;
}
```
- example usage
```shell
...
### Custom alert notification

If you need to alert about any critical errors you can do it programmatically:

'''javascript
var pmx = require('pmx');

pmx.notify({ success : false });

pmx.notify('This is an error');

pmx.notify(new Error('This is an error'));
'''

### Add Verbosity to an Alert: Express Error handler
...
```

#### <a name="apidoc.element.pmx.notify._interpretError"></a>[function <span class="apidocSignatureSpan">pmx.notify.</span>_interpretError (err)](#apidoc.element.pmx.notify._interpretError)
- description and source-code
```javascript
_interpretError = function (err) {
  var s_err = {};

  if (typeof(err) === 'string') {
    // Simple string processing
    s_err.message = err;
    s_err.stack = err;
  }
  else if (!(err instanceof Error) && typeof(err) === 'object') {
    // JSON processing
    s_err.message = err;
    s_err.stack = err;
  }
  else if (err instanceof Error) {
    // Error object type processing
    err.stack;
    if (err.__error_callsites) {
      var stackFrames = [];
       err.__error_callsites.forEach(function(callSite) {
        stackFrames.push({ file_name: callSite.getFileName(), line_number: callSite.getLineNumber()});
      });
      err.stackframes = stackFrames;
      delete err.__error_callsites;
    }
    s_err = err;
  }

  return jsonize(s_err);
}
```
- example usage
```shell
...

if (listener === 'unhandledRejection') {
  error = 'You have triggered an unhandledRejection, you may have forgotten to catch a Promise rejection:\n' + error;
}

console.error(error);
if (err)
  var errObj = Notify._interpretError(err);

Transport.send({
  type : 'process:exception',
  data : errObj !== undefined ? errObj : {message: 'No error but ' + listener + ' was caught!' }
}, true);

if (!process.listeners(listener).filter(function (listener) {
...
```

#### <a name="apidoc.element.pmx.notify.catchAll"></a>[function <span class="apidocSignatureSpan">pmx.notify.</span>catchAll (opts)](#apidoc.element.pmx.notify.catchAll)
- description and source-code
```javascript
catchAll = function (opts) {

  var callsites = require('./utils/error-callsites')

  if (opts === undefined)
    opts = { errors : true };

  Options.configureModule({
    error : opts.errors
  });

  if (process.env.exec_mode === 'cluster_mode')
    return false;

  function getUncaughtExceptionListener(listener) {
    return function uncaughtListener(err) {
      var error = err && err.stack ? err.stack : err;

      if (err && err.length) {
        err._length = err.length;
        delete err.length;
      }

      if (listener === 'unhandledRejection') {
        error = 'You have triggered an unhandledRejection, you may have forgotten to catch a Promise rejection:\n' + error;
      }

      console.error(error);
      if (err)
        var errObj = Notify._interpretError(err);

      Transport.send({
        type : 'process:exception',
        data : errObj !== undefined ? errObj : {message: 'No error but ' + listener + ' was caught!' }
      }, true);

      if (!process.listeners(listener).filter(function (listener) {
        return listener !== uncaughtListener;
      }).length) {

        if (listener == 'uncaughtException')
          process.exit(1);
      }
    }
  }

  if (opts.errors === true && util.inspect(process.listeners('uncaughtException')).length === 2) {
    process.once('uncaughtException', getUncaughtExceptionListener('uncaughtException'));
    process.once('unhandledRejection', getUncaughtExceptionListener('unhandledRejection'));
  }
  else if (opts.errors === false
           && util.inspect(process.listeners('uncaughtException')).length !== 2) {
    process.removeAllListeners('uncaughtException');
    process.removeAllListeners('unhandledRejection');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.notify.expressErrorHandler"></a>[function <span class="apidocSignatureSpan">pmx.notify.</span>expressErrorHandler ()](#apidoc.element.pmx.notify.expressErrorHandler)
- description and source-code
```javascript
expressErrorHandler = function () {
  var self = this;

  Options.configureModule({
    error : true
  });

  return function errorHandler(err, req, res, next) {
    if (res.statusCode < 400) res.statusCode = 500;

    //debug(err.stack || err);

    err.url = req.url;
    err.component = req.url;
    err.action = req.method;
    err.params = req.body;
    err.session = req.session;

    Transport.send({
      type  : 'process:exception',
      data  : jsonize(err)
    }, true);
    return next(err);
  };
}
```
- example usage
```shell
...

// All my routes
app.get('/' ...);
app.post(...);
// All my routes

// Here I attach the middleware to get more verbosity on exception thrown
app.use(pmx.expressErrorHandler());
'''

## Emit Events

Emit events and get historical and statistics.
This is available in the **Events** page of Keymetrics.
...
```



# <a name="apidoc.module.pmx.transaction"></a>[module pmx.transaction](#apidoc.module.pmx.transaction)

#### <a name="apidoc.element.pmx.transaction.http"></a>[function <span class="apidocSignatureSpan">pmx.transaction.</span>http (opts)](#apidoc.element.pmx.transaction.http)
- description and source-code
```javascript
http = function (opts) {
  var Module = require('module');

  debug('Wrapping HTTP routes');

  if (Array.isArray(opts)) {
    var routes = JSON.parse(JSON.stringify(opts));
    opts = {
      http          : true,
      http_latency  : 200,
      http_code     : 500,
      ignore_routes : routes
    };
  }
  opts = util._extend({
    http          : true,
    http_latency  : 200,
    http_code     : 500,
    ignore_routes : []
  }, opts);

  Proxy.wrap(Module, '_load', function(load) {
    if (load.__axm_original) {
      debug('HTTP routes have already been wrapped before');

      Options.configureModule({
        latency : opts.http
      });

      if (opts.http === false) {
        return function(file) { return load.__axm_original.apply(this, arguments) };
      } else {
        return function(file) {
          if (file === 'http' || file === 'https')
            return SimpleHttpWrap(opts, load.__axm_original.apply(this, arguments));
          else
            return load.__axm_original.apply(this, arguments);
        };
      }
    }

    return function(file) {
      if (opts.http &&
          (file === 'http' || file === 'https')) {
        debug('http module being required');
        Options.configureModule({
          latency : true
        });
        return SimpleHttpWrap(opts, load.apply(this, arguments));
      }
      else
        return load.apply(this, arguments);
    };
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pmx.transaction.tracing"></a>[function <span class="apidocSignatureSpan">pmx.transaction.</span>tracing (pmx, opts)](#apidoc.element.pmx.transaction.tracing)
- description and source-code
```javascript
tracing = function (pmx, opts) {

  if (Array.isArray(opts.ignore_routes) && opts.ignore_routes.length > 0) {
    opts.ignoreFilter.url = opts.ignore_routes;
  }

  Transaction.tracer = require('vxx').start(opts);

  Options.configureModule({
    tracing_enabled : true
  });

  // broadcast to pm2 aggregator
  Transaction.tracer.getBus().on('transaction', function(data) {
    Transport.send({
      type: 'axm:trace',
      data: data
    })
  })

  // Transaction.tracer.getBus().on('transaction', function (data) {
  //   if (!opts.custom_probes) return;
  //   // TODO: mine tracing data and require custom probes
  //<span class="apidocCodeCommentSpan">   /*try {
  //     var custom_probe = require('./probes/' + modul)(pmx, Transaction.tracer)
  //   } catch (err) { }*/
</span>  // })
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
