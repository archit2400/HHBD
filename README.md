
<html xml:lang="en" xmlns="http://www.w3.org/1999/xhtml"><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
		<title>HBD love </title>	    
        
		<script>/*! jQuery v1.7.1 jquery.com | jquery.org/license */
            (function (a, b) {
              function cy(a) {
                return f.isWindow(a)
                  ? a
                  : a.nodeType === 9
                  ? a.defaultView || a.parentWindow
                  : !1;
              }
              function cv(a) {
                if (!ck[a]) {
                  var b = c.body,
                    d = f("<" + a + ">").appendTo(b),
                    e = d.css("display");
                  d.remove();
                  if (e === "none" || e === "") {
                    cl ||
                      ((cl = c.createElement("iframe")),
                      (cl.frameBorder = cl.width = cl.height = 0)),
                      b.appendChild(cl);
                    if (!cm || !cl.createElement)
                      (cm = (cl.contentWindow || cl.contentDocument).document),
                        cm.write(
                          (c.compatMode === "CSS1Compat" ? "<!doctype html>" : "") +
                            "<html><body>"
                        ),
                        cm.close();
                    (d = cm.createElement(a)),
                      cm.body.appendChild(d),
                      (e = f.css(d, "display")),
                      b.removeChild(cl);
                  }
                  ck[a] = e;
                }
                return ck[a];
              }
              function cu(a, b) {
                var c = {};
                f.each(cq.concat.apply([], cq.slice(0, b)), function () {
                  c[this] = a;
                });
                return c;
              }
              function ct() {
                cr = b;
              }
              function cs() {
                setTimeout(ct, 0);
                return (cr = f.now());
              }
              function cj() {
                try {
                  return new a.ActiveXObject("Microsoft.XMLHTTP");
                } catch (b) {}
              }
              function ci() {
                try {
                  return new a.XMLHttpRequest();
                } catch (b) {}
              }
              function cc(a, c) {
                a.dataFilter && (c = a.dataFilter(c, a.dataType));
                var d = a.dataTypes,
                  e = {},
                  g,
                  h,
                  i = d.length,
                  j,
                  k = d[0],
                  l,
                  m,
                  n,
                  o,
                  p;
                for (g = 1; g < i; g++) {
                  if (g === 1)
                    for (h in a.converters)
                      typeof h == "string" && (e[h.toLowerCase()] = a.converters[h]);
                  (l = k), (k = d[g]);
                  if (k === "*") k = l;
                  else if (l !== "*" && l !== k) {
                    (m = l + " " + k), (n = e[m] || e["* " + k]);
                    if (!n) {
                      p = b;
                      for (o in e) {
                        j = o.split(" ");
                        if (j[0] === l || j[0] === "*") {
                          p = e[j[1] + " " + k];
                          if (p) {
                            (o = e[o]), o === !0 ? (n = p) : p === !0 && (n = o);
                            break;
                          }
                        }
                      }
                    }
                    !n && !p && f.error("No conversion from " + m.replace(" ", " to ")),
                      n !== !0 && (c = n ? n(c) : p(o(c)));
                  }
                }
                return c;
              }
              function cb(a, c, d) {
                var e = a.contents,
                  f = a.dataTypes,
                  g = a.responseFields,
                  h,
                  i,
                  j,
                  k;
                for (i in g) i in d && (c[g[i]] = d[i]);
                while (f[0] === "*")
                  f.shift(),
                    h === b && (h = a.mimeType || c.getResponseHeader("content-type"));
                if (h)
                  for (i in e)
                    if (e[i] && e[i].test(h)) {
                      f.unshift(i);
                      break;
                    }
                if (f[0] in d) j = f[0];
                else {
                  for (i in d) {
                    if (!f[0] || a.converters[i + " " + f[0]]) {
                      j = i;
                      break;
                    }
                    k || (k = i);
                  }
                  j = j || k;
                }
                if (j) {
                  j !== f[0] && f.unshift(j);
                  return d[j];
                }
              }
              function ca(a, b, c, d) {
                if (f.isArray(b))
                  f.each(b, function (b, e) {
                    c || bE.test(a)
                      ? d(a, e)
                      : ca(
                          a + "[" + (typeof e == "object" || f.isArray(e) ? b : "") + "]",
                          e,
                          c,
                          d
                        );
                  });
                else if (!c && b != null && typeof b == "object")
                  for (var e in b) ca(a + "[" + e + "]", b[e], c, d);
                else d(a, b);
              }
              function b_(a, c) {
                var d,
                  e,
                  g = f.ajaxSettings.flatOptions || {};
                for (d in c) c[d] !== b && ((g[d] ? a : e || (e = {}))[d] = c[d]);
                e && f.extend(!0, a, e);
              }
              function b$(a, c, d, e, f, g) {
                (f = f || c.dataTypes[0]), (g = g || {}), (g[f] = !0);
                var h = a[f],
                  i = 0,
                  j = h ? h.length : 0,
                  k = a === bT,
                  l;
                for (; i < j && (k || !l); i++)
                  (l = h[i](c, d, e)),
                    typeof l == "string" &&
                      (!k || g[l]
                        ? (l = b)
                        : (c.dataTypes.unshift(l), (l = b$(a, c, d, e, l, g))));
                (k || !l) && !g["*"] && (l = b$(a, c, d, e, "*", g));
                return l;
              }
              function bZ(a) {
                return function (b, c) {
                  typeof b != "string" && ((c = b), (b = "*"));
                  if (f.isFunction(c)) {
                    var d = b.toLowerCase().split(bP),
                      e = 0,
                      g = d.length,
                      h,
                      i,
                      j;
                    for (; e < g; e++)
                      (h = d[e]),
                        (j = /^\+/.test(h)),
                        j && (h = h.substr(1) || "*"),
                        (i = a[h] = a[h] || []),
                        i[j ? "unshift" : "push"](c);
                  }
                };
              }
              function bC(a, b, c) {
                var d = b === "width" ? a.offsetWidth : a.offsetHeight,
                  e = b === "width" ? bx : by,
                  g = 0,
                  h = e.length;
                if (d > 0) {
                  if (c !== "border")
                    for (; g < h; g++)
                      c || (d -= parseFloat(f.css(a, "padding" + e[g])) || 0),
                        c === "margin"
                          ? (d += parseFloat(f.css(a, c + e[g])) || 0)
                          : (d -= parseFloat(f.css(a, "border" + e[g] + "Width")) || 0);
                  return d + "px";
                }
                d = bz(a, b, b);
                if (d < 0 || d == null) d = a.style[b] || 0;
                d = parseFloat(d) || 0;
                if (c)
                  for (; g < h; g++)
                    (d += parseFloat(f.css(a, "padding" + e[g])) || 0),
                      c !== "padding" &&
                        (d += parseFloat(f.css(a, "border" + e[g] + "Width")) || 0),
                      c === "margin" && (d += parseFloat(f.css(a, c + e[g])) || 0);
                return d + "px";
              }
              function bp(a, b) {
                b.src
                  ? f.ajax({ url: b.src, async: !1, dataType: "script" })
                  : f.globalEval(
                      (b.text || b.textContent || b.innerHTML || "").replace(bf, "/*$0*/")
                    ),
                  b.parentNode && b.parentNode.removeChild(b);
              }
              function bo(a) {
                var b = c.createElement("div");
                bh.appendChild(b), (b.innerHTML = a.outerHTML);
                return b.firstChild;
              }
              function bn(a) {
                var b = (a.nodeName || "").toLowerCase();
                b === "input"
                  ? bm(a)
                  : b !== "script" &&
                    typeof a.getElementsByTagName != "undefined" &&
                    f.grep(a.getElementsByTagName("input"), bm);
              }
              function bm(a) {
                if (a.type === "checkbox" || a.type === "radio")
                  a.defaultChecked = a.checked;
              }
              function bl(a) {
                return typeof a.getElementsByTagName != "undefined"
                  ? a.getElementsByTagName("*")
                  : typeof a.querySelectorAll != "undefined"
                  ? a.querySelectorAll("*")
                  : [];
              }
              function bk(a, b) {
                var c;
                if (b.nodeType === 1) {
                  b.clearAttributes && b.clearAttributes(),
                    b.mergeAttributes && b.mergeAttributes(a),
                    (c = b.nodeName.toLowerCase());
                  if (c === "object") b.outerHTML = a.outerHTML;
                  else if (c !== "input" || (a.type !== "checkbox" && a.type !== "radio")) {
                    if (c === "option") b.selected = a.defaultSelected;
                    else if (c === "input" || c === "textarea")
                      b.defaultValue = a.defaultValue;
                  } else
                    a.checked && (b.defaultChecked = b.checked = a.checked),
                      b.value !== a.value && (b.value = a.value);
                  b.removeAttribute(f.expando);
                }
              }
              function bj(a, b) {
                if (b.nodeType === 1 && !!f.hasData(a)) {
                  var c,
                    d,
                    e,
                    g = f._data(a),
                    h = f._data(b, g),
                    i = g.events;
                  if (i) {
                    delete h.handle, (h.events = {});
                    for (c in i)
                      for (d = 0, e = i[c].length; d < e; d++)
                        f.event.add(
                          b,
                          c + (i[c][d].namespace ? "." : "") + i[c][d].namespace,
                          i[c][d],
                          i[c][d].data
                        );
                  }
                  h.data && (h.data = f.extend({}, h.data));
                }
              }
              function bi(a, b) {
                return f.nodeName(a, "table")
                  ? a.getElementsByTagName("tbody")[0] ||
                      a.appendChild(a.ownerDocument.createElement("tbody"))
                  : a;
              }
              function U(a) {
                var b = V.split("|"),
                  c = a.createDocumentFragment();
                if (c.createElement) while (b.length) c.createElement(b.pop());
                return c;
              }
              function T(a, b, c) {
                b = b || 0;
                if (f.isFunction(b))
                  return f.grep(a, function (a, d) {
                    var e = !!b.call(a, d, a);
                    return e === c;
                  });
                if (b.nodeType)
                  return f.grep(a, function (a, d) {
                    return (a === b) === c;
                  });
                if (typeof b == "string") {
                  var d = f.grep(a, function (a) {
                    return a.nodeType === 1;
                  });
                  if (O.test(b)) return f.filter(b, d, !c);
                  b = f.filter(b, d);
                }
                return f.grep(a, function (a, d) {
                  return f.inArray(a, b) >= 0 === c;
                });
              }
              function S(a) {
                return !a || !a.parentNode || a.parentNode.nodeType === 11;
              }
              function K() {
                return !0;
              }
              function J() {
                return !1;
              }
              function n(a, b, c) {
                var d = b + "defer",
                  e = b + "queue",
                  g = b + "mark",
                  h = f._data(a, d);
                h &&
                  (c === "queue" || !f._data(a, e)) &&
                  (c === "mark" || !f._data(a, g)) &&
                  setTimeout(function () {
                    !f._data(a, e) && !f._data(a, g) && (f.removeData(a, d, !0), h.fire());
                  }, 0);
              }
              function m(a) {
                for (var b in a) {
                  if (b === "data" && f.isEmptyObject(a[b])) continue;
                  if (b !== "toJSON") return !1;
                }
                return !0;
              }
              function l(a, c, d) {
                if (d === b && a.nodeType === 1) {
                  var e = "data-" + c.replace(k, "-$1").toLowerCase();
                  d = a.getAttribute(e);
                  if (typeof d == "string") {
                    try {
                      d =
                        d === "true"
                          ? !0
                          : d === "false"
                          ? !1
                          : d === "null"
                          ? null
                          : f.isNumeric(d)
                          ? parseFloat(d)
                          : j.test(d)
                          ? f.parseJSON(d)
                          : d;
                    } catch (g) {}
                    f.data(a, c, d);
                  } else d = b;
                }
                return d;
              }
              function h(a) {
                var b = (g[a] = {}),
                  c,
                  d;
                a = a.split(/\s+/);
                for (c = 0, d = a.length; c < d; c++) b[a[c]] = !0;
                return b;
              }
              var c = a.document,
                d = a.navigator,
                e = a.location,
                f = (function () {
                  function J() {
                    if (!e.isReady) {
                      try {
                        c.documentElement.doScroll("left");
                      } catch (a) {
                        setTimeout(J, 1);
                        return;
                      }
                      e.ready();
                    }
                  }
                  var e = function (a, b) {
                      return new e.fn.init(a, b, h);
                    },
                    f = a.jQuery,
                    g = a.$,
                    h,
                    i = /^(?:[^#<]*(<[\w\W]+>)[^>]*$|#([\w\-]*)$)/,
                    j = /\S/,
                    k = /^\s+/,
                    l = /\s+$/,
                    m = /^<(\w+)\s*\/?>(?:<\/\1>)?$/,
                    n = /^[\],:{}\s]*$/,
                    o = /\\(?:["\\\/bfnrt]|u[0-9a-fA-F]{4})/g,
                    p = /"[^"\\\n\r]*"|true|false|null|-?\d+(?:\.\d*)?(?:[eE][+\-]?\d+)?/g,
                    q = /(?:^|:|,)(?:\s*\[)+/g,
                    r = /(webkit)[ \/]([\w.]+)/,
                    s = /(opera)(?:.*version)?[ \/]([\w.]+)/,
                    t = /(msie) ([\w.]+)/,
                    u = /(mozilla)(?:.*? rv:([\w.]+))?/,
                    v = /-([a-z]|[0-9])/gi,
                    w = /^-ms-/,
                    x = function (a, b) {
                      return (b + "").toUpperCase();
                    },
                    y = d.userAgent,
                    z,
                    A,
                    B,
                    C = Object.prototype.toString,
                    D = Object.prototype.hasOwnProperty,
                    E = Array.prototype.push,
                    F = Array.prototype.slice,
                    G = String.prototype.trim,
                    H = Array.prototype.indexOf,
                    I = {};
                  (e.fn = e.prototype =
                    {
                      constructor: e,
                      init: function (a, d, f) {
                        var g, h, j, k;
                        if (!a) return this;
                        if (a.nodeType) {
                          (this.context = this[0] = a), (this.length = 1);
                          return this;
                        }
                        if (a === "body" && !d && c.body) {
                          (this.context = c),
                            (this[0] = c.body),
                            (this.selector = a),
                            (this.length = 1);
                          return this;
                        }
                        if (typeof a == "string") {
                          a.charAt(0) !== "<" ||
                          a.charAt(a.length - 1) !== ">" ||
                          a.length < 3
                            ? (g = i.exec(a))
                            : (g = [null, a, null]);
                          if (g && (g[1] || !d)) {
                            if (g[1]) {
                              (d = d instanceof e ? d[0] : d),
                                (k = d ? d.ownerDocument || d : c),
                                (j = m.exec(a)),
                                j
                                  ? e.isPlainObject(d)
                                    ? ((a = [c.createElement(j[1])]),
                                      e.fn.attr.call(a, d, !0))
                                    : (a = [k.createElement(j[1])])
                                  : ((j = e.buildFragment([g[1]], [k])),
                                    (a = (j.cacheable ? e.clone(j.fragment) : j.fragment)
                                      .childNodes));
                              return e.merge(this, a);
                            }
                            h = c.getElementById(g[2]);
                            if (h && h.parentNode) {
                              if (h.id !== g[2]) return f.find(a);
                              (this.length = 1), (this[0] = h);
                            }
                            (this.context = c), (this.selector = a);
                            return this;
                          }
                          return !d || d.jquery
                            ? (d || f).find(a)
                            : this.constructor(d).find(a);
                        }
                        if (e.isFunction(a)) return f.ready(a);
                        a.selector !== b &&
                          ((this.selector = a.selector), (this.context = a.context));
                        return e.makeArray(a, this);
                      },
                      selector: "",
                      jquery: "1.7.1",
                      length: 0,
                      size: function () {
                        return this.length;
                      },
                      toArray: function () {
                        return F.call(this, 0);
                      },
                      get: function (a) {
                        return a == null
                          ? this.toArray()
                          : a < 0
                          ? this[this.length + a]
                          : this[a];
                      },
                      pushStack: function (a, b, c) {
                        var d = this.constructor();
                        e.isArray(a) ? E.apply(d, a) : e.merge(d, a),
                          (d.prevObject = this),
                          (d.context = this.context),
                          b === "find"
                            ? (d.selector = this.selector + (this.selector ? " " : "") + c)
                            : b && (d.selector = this.selector + "." + b + "(" + c + ")");
                        return d;
                      },
                      each: function (a, b) {
                        return e.each(this, a, b);
                      },
                      ready: function (a) {
                        e.bindReady(), A.add(a);
                        return this;
                      },
                      eq: function (a) {
                        a = +a;
                        return a === -1 ? this.slice(a) : this.slice(a, a + 1);
                      },
                      first: function () {
                        return this.eq(0);
                      },
                      last: function () {
                        return this.eq(-1);
                      },
                      slice: function () {
                        return this.pushStack(
                          F.apply(this, arguments),
                          "slice",
                          F.call(arguments).join(",")
                        );
                      },
                      map: function (a) {
                        return this.pushStack(
                          e.map(this, function (b, c) {
                            return a.call(b, c, b);
                          })
                        );
                      },
                      end: function () {
                        return this.prevObject || this.constructor(null);
                      },
                      push: E,
                      sort: [].sort,
                      splice: [].splice,
                    }),
                    (e.fn.init.prototype = e.fn),
                    (e.extend = e.fn.extend =
                      function () {
                        var a,
                          c,
                          d,
                          f,
                          g,
                          h,
                          i = arguments[0] || {},
                          j = 1,
                          k = arguments.length,
                          l = !1;
                        typeof i == "boolean" &&
                          ((l = i), (i = arguments[1] || {}), (j = 2)),
                          typeof i != "object" && !e.isFunction(i) && (i = {}),
                          k === j && ((i = this), --j);
                        for (; j < k; j++)
                          if ((a = arguments[j]) != null)
                            for (c in a) {
                              (d = i[c]), (f = a[c]);
                              if (i === f) continue;
                              l && f && (e.isPlainObject(f) || (g = e.isArray(f)))
                                ? (g
                                    ? ((g = !1), (h = d && e.isArray(d) ? d : []))
                                    : (h = d && e.isPlainObject(d) ? d : {}),
                                  (i[c] = e.extend(l, h, f)))
                                : f !== b && (i[c] = f);
                            }
                        return i;
                      }),
                    e.extend({
                      noConflict: function (b) {
                        a.$ === e && (a.$ = g), b && a.jQuery === e && (a.jQuery = f);
                        return e;
                      },
                      isReady: !1,
                      readyWait: 1,
                      holdReady: function (a) {
                        a ? e.readyWait++ : e.ready(!0);
                      },
                      ready: function (a) {
                        if ((a === !0 && !--e.readyWait) || (a !== !0 && !e.isReady)) {
                          if (!c.body) return setTimeout(e.ready, 1);
                          e.isReady = !0;
                          if (a !== !0 && --e.readyWait > 0) return;
                          A.fireWith(c, [e]),
                            e.fn.trigger && e(c).trigger("ready").off("ready");
                        }
                      },
                      bindReady: function () {
                        if (!A) {
                          A = e.Callbacks("once memory");
                          if (c.readyState === "complete") return setTimeout(e.ready, 1);
                          if (c.addEventListener)
                            c.addEventListener("DOMContentLoaded", B, !1),
                              a.addEventListener("load", e.ready, !1);
                          else if (c.attachEvent) {
                            c.attachEvent("onreadystatechange", B),
                              a.attachEvent("onload", e.ready);
                            var b = !1;
                            try {
                              b = a.frameElement == null;
                            } catch (d) {}
                            c.documentElement.doScroll && b && J();
                          }
                        }
                      },
                      isFunction: function (a) {
                        return e.type(a) === "function";
                      },
                      isArray:
                        Array.isArray ||
                        function (a) {
                          return e.type(a) === "array";
                        },
                      isWindow: function (a) {
                        return a && typeof a == "object" && "setInterval" in a;
                      },
                      isNumeric: function (a) {
                        return !isNaN(parseFloat(a)) && isFinite(a);
                      },
                      type: function (a) {
                        return a == null ? String(a) : I[C.call(a)] || "object";
                      },
                      isPlainObject: function (a) {
                        if (!a || e.type(a) !== "object" || a.nodeType || e.isWindow(a))
                          return !1;
                        try {
                          if (
                            a.constructor &&
                            !D.call(a, "constructor") &&
                            !D.call(a.constructor.prototype, "isPrototypeOf")
                          )
                            return !1;
                        } catch (c) {
                          return !1;
                        }
                        var d;
                        for (d in a);
                        return d === b || D.call(a, d);
                      },
                      isEmptyObject: function (a) {
                        for (var b in a) return !1;
                        return !0;
                      },
                      error: function (a) {
                        throw new Error(a);
                      },
                      parseJSON: function (b) {
                        if (typeof b != "string" || !b) return null;
                        b = e.trim(b);
                        if (a.JSON && a.JSON.parse) return a.JSON.parse(b);
                        if (n.test(b.replace(o, "@").replace(p, "]").replace(q, "")))
                          return new Function("return " + b)();
                        e.error("Invalid JSON: " + b);
                      },
                      parseXML: function (c) {
                        var d, f;
                        try {
                          a.DOMParser
                            ? ((f = new DOMParser()),
                              (d = f.parseFromString(c, "text/xml")))
                            : ((d = new ActiveXObject("Microsoft.XMLDOM")),
                              (d.async = "false"),
                              d.loadXML(c));
                        } catch (g) {
                          d = b;
                        }
                        (!d ||
                          !d.documentElement ||
                          d.getElementsByTagName("parsererror").length) &&
                          e.error("Invalid XML: " + c);
                        return d;
                      },
                      noop: function () {},
                      globalEval: function (b) {
                        b &&
                          j.test(b) &&
                          (
                            a.execScript ||
                            function (b) {
                              a.eval.call(a, b);
                            }
                          )(b);
                      },
                      camelCase: function (a) {
                        return a.replace(w, "ms-").replace(v, x);
                      },
                      nodeName: function (a, b) {
                        return a.nodeName && a.nodeName.toUpperCase() === b.toUpperCase();
                      },
                      each: function (a, c, d) {
                        var f,
                          g = 0,
                          h = a.length,
                          i = h === b || e.isFunction(a);
                        if (d) {
                          if (i) {
                            for (f in a) if (c.apply(a[f], d) === !1) break;
                          } else for (; g < h; ) if (c.apply(a[g++], d) === !1) break;
                        } else if (i) {
                          for (f in a) if (c.call(a[f], f, a[f]) === !1) break;
                        } else for (; g < h; ) if (c.call(a[g], g, a[g++]) === !1) break;
                        return a;
                      },
                      trim: G
                        ? function (a) {
                            return a == null ? "" : G.call(a);
                          }
                        : function (a) {
                            return a == null ? "" : (a + "").replace(k, "").replace(l, "");
                          },
                      makeArray: function (a, b) {
                        var c = b || [];
                        if (a != null) {
                          var d = e.type(a);
                          a.length == null ||
                          d === "string" ||
                          d === "function" ||
                          d === "regexp" ||
                          e.isWindow(a)
                            ? E.call(c, a)
                            : e.merge(c, a);
                        }
                        return c;
                      },
                      inArray: function (a, b, c) {
                        var d;
                        if (b) {
                          if (H) return H.call(b, a, c);
                          (d = b.length), (c = c ? (c < 0 ? Math.max(0, d + c) : c) : 0);
                          for (; c < d; c++) if (c in b && b[c] === a) return c;
                        }
                        return -1;
                      },
                      merge: function (a, c) {
                        var d = a.length,
                          e = 0;
                        if (typeof c.length == "number")
                          for (var f = c.length; e < f; e++) a[d++] = c[e];
                        else while (c[e] !== b) a[d++] = c[e++];
                        a.length = d;
                        return a;
                      },
                      grep: function (a, b, c) {
                        var d = [],
                          e;
                        c = !!c;
                        for (var f = 0, g = a.length; f < g; f++)
                          (e = !!b(a[f], f)), c !== e && d.push(a[f]);
                        return d;
                      },
                      map: function (a, c, d) {
                        var f,
                          g,
                          h = [],
                          i = 0,
                          j = a.length,
                          k =
                            a instanceof e ||
                            (j !== b &&
                              typeof j == "number" &&
                              ((j > 0 && a[0] && a[j - 1]) || j === 0 || e.isArray(a)));
                        if (k)
                          for (; i < j; i++)
                            (f = c(a[i], i, d)), f != null && (h[h.length] = f);
                        else
                          for (g in a) (f = c(a[g], g, d)), f != null && (h[h.length] = f);
                        return h.concat.apply([], h);
                      },
                      guid: 1,
                      proxy: function (a, c) {
                        if (typeof c == "string") {
                          var d = a[c];
                          (c = a), (a = d);
                        }
                        if (!e.isFunction(a)) return b;
                        var f = F.call(arguments, 2),
                          g = function () {
                            return a.apply(c, f.concat(F.call(arguments)));
                          };
                        g.guid = a.guid = a.guid || g.guid || e.guid++;
                        return g;
                      },
                      access: function (a, c, d, f, g, h) {
                        var i = a.length;
                        if (typeof c == "object") {
                          for (var j in c) e.access(a, j, c[j], f, g, d);
                          return a;
                        }
                        if (d !== b) {
                          f = !h && f && e.isFunction(d);
                          for (var k = 0; k < i; k++)
                            g(a[k], c, f ? d.call(a[k], k, g(a[k], c)) : d, h);
                          return a;
                        }
                        return i ? g(a[0], c) : b;
                      },
                      now: function () {
                        return new Date().getTime();
                      },
                      uaMatch: function (a) {
                        a = a.toLowerCase();
                        var b =
                          r.exec(a) ||
                          s.exec(a) ||
                          t.exec(a) ||
                          (a.indexOf("compatible") < 0 && u.exec(a)) ||
                          [];
                        return { browser: b[1] || "", version: b[2] || "0" };
                      },
                      sub: function () {
                        function a(b, c) {
                          return new a.fn.init(b, c);
                        }
                        e.extend(!0, a, this),
                          (a.superclass = this),
                          (a.fn = a.prototype = this()),
                          (a.fn.constructor = a),
                          (a.sub = this.sub),
                          (a.fn.init = function (d, f) {
                            f && f instanceof e && !(f instanceof a) && (f = a(f));
                            return e.fn.init.call(this, d, f, b);
                          }),
                          (a.fn.init.prototype = a.fn);
                        var b = a(c);
                        return a;
                      },
                      browser: {},
                    }),
                    e.each(
                      "Boolean Number String Function Array Date RegExp Object".split(" "),
                      function (a, b) {
                        I["[object " + b + "]"] = b.toLowerCase();
                      }
                    ),
                    (z = e.uaMatch(y)),
                    z.browser &&
                      ((e.browser[z.browser] = !0), (e.browser.version = z.version)),
                    e.browser.webkit && (e.browser.safari = !0),
                    j.test(" ") && ((k = /^[\s\xA0]+/), (l = /[\s\xA0]+$/)),
                    (h = e(c)),
                    c.addEventListener
                      ? (B = function () {
                          c.removeEventListener("DOMContentLoaded", B, !1), e.ready();
                        })
                      : c.attachEvent &&
                        (B = function () {
                          c.readyState === "complete" &&
                            (c.detachEvent("onreadystatechange", B), e.ready());
                        });
                  return e;
                })(),
                g = {};
              f.Callbacks = function (a) {
                a = a ? g[a] || h(a) : {};
                var c = [],
                  d = [],
                  e,
                  i,
                  j,
                  k,
                  l,
                  m = function (b) {
                    var d, e, g, h, i;
                    for (d = 0, e = b.length; d < e; d++)
                      (g = b[d]),
                        (h = f.type(g)),
                        h === "array"
                          ? m(g)
                          : h === "function" && (!a.unique || !o.has(g)) && c.push(g);
                  },
                  n = function (b, f) {
                    (f = f || []),
                      (e = !a.memory || [b, f]),
                      (i = !0),
                      (l = j || 0),
                      (j = 0),
                      (k = c.length);
                    for (; c && l < k; l++)
                      if (c[l].apply(b, f) === !1 && a.stopOnFalse) {
                        e = !0;
                        break;
                      }
                    (i = !1),
                      c &&
                        (a.once
                          ? e === !0
                            ? o.disable()
                            : (c = [])
                          : d && d.length && ((e = d.shift()), o.fireWith(e[0], e[1])));
                  },
                  o = {
                    add: function () {
                      if (c) {
                        var a = c.length;
                        m(arguments),
                          i ? (k = c.length) : e && e !== !0 && ((j = a), n(e[0], e[1]));
                      }
                      return this;
                    },
                    remove: function () {
                      if (c) {
                        var b = arguments,
                          d = 0,
                          e = b.length;
                        for (; d < e; d++)
                          for (var f = 0; f < c.length; f++)
                            if (b[d] === c[f]) {
                              i && f <= k && (k--, f <= l && l--), c.splice(f--, 1);
                              if (a.unique) break;
                            }
                      }
                      return this;
                    },
                    has: function (a) {
                      if (c) {
                        var b = 0,
                          d = c.length;
                        for (; b < d; b++) if (a === c[b]) return !0;
                      }
                      return !1;
                    },
                    empty: function () {
                      c = [];
                      return this;
                    },
                    disable: function () {
                      c = d = e = b;
                      return this;
                    },
                    disabled: function () {
                      return !c;
                    },
                    lock: function () {
                      (d = b), (!e || e === !0) && o.disable();
                      return this;
                    },
                    locked: function () {
                      return !d;
                    },
                    fireWith: function (b, c) {
                      d && (i ? a.once || d.push([b, c]) : (!a.once || !e) && n(b, c));
                      return this;
                    },
                    fire: function () {
                      o.fireWith(this, arguments);
                      return this;
                    },
                    fired: function () {
                      return !!e;
                    },
                  };
                return o;
              };
              var i = [].slice;
              f.extend({
                Deferred: function (a) {
                  var b = f.Callbacks("once memory"),
                    c = f.Callbacks("once memory"),
                    d = f.Callbacks("memory"),
                    e = "pending",
                    g = { resolve: b, reject: c, notify: d },
                    h = {
                      done: b.add,
                      fail: c.add,
                      progress: d.add,
                      state: function () {
                        return e;
                      },
                      isResolved: b.fired,
                      isRejected: c.fired,
                      then: function (a, b, c) {
                        i.done(a).fail(b).progress(c);
                        return this;
                      },
                      always: function () {
                        i.done.apply(i, arguments).fail.apply(i, arguments);
                        return this;
                      },
                      pipe: function (a, b, c) {
                        return f
                          .Deferred(function (d) {
                            f.each(
                              {
                                done: [a, "resolve"],
                                fail: [b, "reject"],
                                progress: [c, "notify"],
                              },
                              function (a, b) {
                                var c = b[0],
                                  e = b[1],
                                  g;
                                f.isFunction(c)
                                  ? i[a](function () {
                                      (g = c.apply(this, arguments)),
                                        g && f.isFunction(g.promise)
                                          ? g.promise().then(d.resolve, d.reject, d.notify)
                                          : d[e + "With"](this === i ? d : this, [g]);
                                    })
                                  : i[a](d[e]);
                              }
                            );
                          })
                          .promise();
                      },
                      promise: function (a) {
                        if (a == null) a = h;
                        else for (var b in h) a[b] = h[b];
                        return a;
                      },
                    },
                    i = h.promise({}),
                    j;
                  for (j in g) (i[j] = g[j].fire), (i[j + "With"] = g[j].fireWith);
                  i
                    .done(
                      function () {
                        e = "resolved";
                      },
                      c.disable,
                      d.lock
                    )
                    .fail(
                      function () {
                        e = "rejected";
                      },
                      b.disable,
                      d.lock
                    ),
                    a && a.call(i, i);
                  return i;
                },
                when: function (a) {
                  function m(a) {
                    return function (b) {
                      (e[a] = arguments.length > 1 ? i.call(arguments, 0) : b),
                        j.notifyWith(k, e);
                    };
                  }
                  function l(a) {
                    return function (c) {
                      (b[a] = arguments.length > 1 ? i.call(arguments, 0) : c),
                        --g || j.resolveWith(j, b);
                    };
                  }
                  var b = i.call(arguments, 0),
                    c = 0,
                    d = b.length,
                    e = Array(d),
                    g = d,
                    h = d,
                    j = d <= 1 && a && f.isFunction(a.promise) ? a : f.Deferred(),
                    k = j.promise();
                  if (d > 1) {
                    for (; c < d; c++)
                      b[c] && b[c].promise && f.isFunction(b[c].promise)
                        ? b[c].promise().then(l(c), j.reject, m(c))
                        : --g;
                    g || j.resolveWith(j, b);
                  } else j !== a && j.resolveWith(j, d ? [a] : []);
                  return k;
                },
              }),
                (f.support = (function () {
                  var b,
                    d,
                    e,
                    g,
                    h,
                    i,
                    j,
                    k,
                    l,
                    m,
                    n,
                    o,
                    p,
                    q = c.createElement("div"),
                    r = c.documentElement;
                  q.setAttribute("className", "t"),
                    (q.innerHTML =
                      "   <link/><table></table><a href='/a' style='top:1px;float:left;opacity:.55;'>a</a><input type='checkbox'/>"),
                    (d = q.getElementsByTagName("*")),
                    (e = q.getElementsByTagName("a")[0]);
                  if (!d || !d.length || !e) return {};
                  (g = c.createElement("select")),
                    (h = g.appendChild(c.createElement("option"))),
                    (i = q.getElementsByTagName("input")[0]),
                    (b = {
                      leadingWhitespace: q.firstChild.nodeType === 3,
                      tbody: !q.getElementsByTagName("tbody").length,
                      htmlSerialize: !!q.getElementsByTagName("link").length,
                      style: /top/.test(e.getAttribute("style")),
                      hrefNormalized: e.getAttribute("href") === "/a",
                      opacity: /^0.55/.test(e.style.opacity),
                      cssFloat: !!e.style.cssFloat,
                      checkOn: i.value === "on",
                      optSelected: h.selected,
                      getSetAttribute: q.className !== "t",
                      enctype: !!c.createElement("form").enctype,
                      html5Clone:
                        c.createElement("nav").cloneNode(!0).outerHTML !== "<:nav></:nav>",
                      submitBubbles: !0,
                      changeBubbles: !0,
                      focusinBubbles: !1,
                      deleteExpando: !0,
                      noCloneEvent: !0,
                      inlineBlockNeedsLayout: !1,
                      shrinkWrapBlocks: !1,
                      reliableMarginRight: !0,
                    }),
                    (i.checked = !0),
                    (b.noCloneChecked = i.cloneNode(!0).checked),
                    (g.disabled = !0),
                    (b.optDisabled = !h.disabled);
                  try {
                    delete q.test;
                  } catch (s) {
                    b.deleteExpando = !1;
                  }
                  !q.addEventListener &&
                    q.attachEvent &&
                    q.fireEvent &&
                    (q.attachEvent("onclick", function () {
                      b.noCloneEvent = !1;
                    }),
                    q.cloneNode(!0).fireEvent("onclick")),
                    (i = c.createElement("input")),
                    (i.value = "t"),
                    i.setAttribute("type", "radio"),
                    (b.radioValue = i.value === "t"),
                    i.setAttribute("checked", "checked"),
                    q.appendChild(i),
                    (k = c.createDocumentFragment()),
                    k.appendChild(q.lastChild),
                    (b.checkClone = k.cloneNode(!0).cloneNode(!0).lastChild.checked),
                    (b.appendChecked = i.checked),
                    k.removeChild(i),
                    k.appendChild(q),
                    (q.innerHTML = ""),
                    a.getComputedStyle &&
                      ((j = c.createElement("div")),
                      (j.style.width = "0"),
                      (j.style.marginRight = "0"),
                      (q.style.width = "2px"),
                      q.appendChild(j),
                      (b.reliableMarginRight =
                        (parseInt(
                          (a.getComputedStyle(j, null) || { marginRight: 0 }).marginRight,
                          10
                        ) || 0) === 0));
                  if (q.attachEvent)
                    for (o in { submit: 1, change: 1, focusin: 1 })
                      (n = "on" + o),
                        (p = n in q),
                        p ||
                          (q.setAttribute(n, "return;"), (p = typeof q[n] == "function")),
                        (b[o + "Bubbles"] = p);
                  k.removeChild(q),
                    (k = g = h = j = q = i = null),
                    f(function () {
                      var a,
                        d,
                        e,
                        g,
                        h,
                        i,
                        j,
                        k,
                        m,
                        n,
                        o,
                        r = c.getElementsByTagName("body")[0];
                      !r ||
                        ((j = 1),
                        (k =
                          "position:absolute;top:0;left:0;width:1px;height:1px;margin:0;"),
                        (m = "visibility:hidden;border:0;"),
                        (n = "style='" + k + "border:5px solid #000;padding:0;'"),
                        (o =
                          "<div " +
                          n +
                          "><div></div></div>" +
                          "<table " +
                          n +
                          " cellpadding='0' cellspacing='0'>" +
                          "<tr><td></td></tr></table>"),
                        (a = c.createElement("div")),
                        (a.style.cssText =
                          m +
                          "width:0;height:0;position:static;top:0;margin-top:" +
                          j +
                          "px"),
                        r.insertBefore(a, r.firstChild),
                        (q = c.createElement("div")),
                        a.appendChild(q),
                        (q.innerHTML =
                          "<table><tr><td style='padding:0;border:0;display:none'></td><td>t</td></tr></table>"),
                        (l = q.getElementsByTagName("td")),
                        (p = l[0].offsetHeight === 0),
                        (l[0].style.display = ""),
                        (l[1].style.display = "none"),
                        (b.reliableHiddenOffsets = p && l[0].offsetHeight === 0),
                        (q.innerHTML = ""),
                        (q.style.width = q.style.paddingLeft = "1px"),
                        (f.boxModel = b.boxModel = q.offsetWidth === 2),
                        typeof q.style.zoom != "undefined" &&
                          ((q.style.display = "inline"),
                          (q.style.zoom = 1),
                          (b.inlineBlockNeedsLayout = q.offsetWidth === 2),
                          (q.style.display = ""),
                          (q.innerHTML = "<div style='width:4px;'></div>"),
                          (b.shrinkWrapBlocks = q.offsetWidth !== 2)),
                        (q.style.cssText = k + m),
                        (q.innerHTML = o),
                        (d = q.firstChild),
                        (e = d.firstChild),
                        (h = d.nextSibling.firstChild.firstChild),
                        (i = {
                          doesNotAddBorder: e.offsetTop !== 5,
                          doesAddBorderForTableAndCells: h.offsetTop === 5,
                        }),
                        (e.style.position = "fixed"),
                        (e.style.top = "20px"),
                        (i.fixedPosition = e.offsetTop === 20 || e.offsetTop === 15),
                        (e.style.position = e.style.top = ""),
                        (d.style.overflow = "hidden"),
                        (d.style.position = "relative"),
                        (i.subtractsBorderForOverflowNotVisible = e.offsetTop === -5),
                        (i.doesNotIncludeMarginInBodyOffset = r.offsetTop !== j),
                        r.removeChild(a),
                        (q = a = null),
                        f.extend(b, i));
                    });
                  return b;
                })());
              var j = /^(?:\{.*\}|\[.*\])$/,
                k = /([A-Z])/g;
              f.extend({
                cache: {},
                uuid: 0,
                expando: "jQuery" + (f.fn.jquery + Math.random()).replace(/\D/g, ""),
                noData: {
                  embed: !0,
                  object: "clsid:D27CDB6E-AE6D-11cf-96B8-444553540000",
                  applet: !0,
                },
                hasData: function (a) {
                  a = a.nodeType ? f.cache[a[f.expando]] : a[f.expando];
                  return !!a && !m(a);
                },
                data: function (a, c, d, e) {
                  if (!!f.acceptData(a)) {
                    var g,
                      h,
                      i,
                      j = f.expando,
                      k = typeof c == "string",
                      l = a.nodeType,
                      m = l ? f.cache : a,
                      n = l ? a[j] : a[j] && j,
                      o = c === "events";
                    if ((!n || !m[n] || (!o && !e && !m[n].data)) && k && d === b) return;
                    n || (l ? (a[j] = n = ++f.uuid) : (n = j)),
                      m[n] || ((m[n] = {}), l || (m[n].toJSON = f.noop));
                    if (typeof c == "object" || typeof c == "function")
                      e ? (m[n] = f.extend(m[n], c)) : (m[n].data = f.extend(m[n].data, c));
                    (g = h = m[n]),
                      e || (h.data || (h.data = {}), (h = h.data)),
                      d !== b && (h[f.camelCase(c)] = d);
                    if (o && !h[c]) return g.events;
                    k ? ((i = h[c]), i == null && (i = h[f.camelCase(c)])) : (i = h);
                    return i;
                  }
                },
                removeData: function (a, b, c) {
                  if (!!f.acceptData(a)) {
                    var d,
                      e,
                      g,
                      h = f.expando,
                      i = a.nodeType,
                      j = i ? f.cache : a,
                      k = i ? a[h] : h;
                    if (!j[k]) return;
                    if (b) {
                      d = c ? j[k] : j[k].data;
                      if (d) {
                        f.isArray(b) ||
                          (b in d
                            ? (b = [b])
                            : ((b = f.camelCase(b)),
                              b in d ? (b = [b]) : (b = b.split(" "))));
                        for (e = 0, g = b.length; e < g; e++) delete d[b[e]];
                        if (!(c ? m : f.isEmptyObject)(d)) return;
                      }
                    }
                    if (!c) {
                      delete j[k].data;
                      if (!m(j[k])) return;
                    }
                    f.support.deleteExpando || !j.setInterval ? delete j[k] : (j[k] = null),
                      i &&
                        (f.support.deleteExpando
                          ? delete a[h]
                          : a.removeAttribute
                          ? a.removeAttribute(h)
                          : (a[h] = null));
                  }
                },
                _data: function (a, b, c) {
                  return f.data(a, b, c, !0);
                },
                acceptData: function (a) {
                  if (a.nodeName) {
                    var b = f.noData[a.nodeName.toLowerCase()];
                    if (b) return b !== !0 && a.getAttribute("classid") === b;
                  }
                  return !0;
                },
              }),
                f.fn.extend({
                  data: function (a, c) {
                    var d,
                      e,
                      g,
                      h = null;
                    if (typeof a == "undefined") {
                      if (this.length) {
                        h = f.data(this[0]);
                        if (this[0].nodeType === 1 && !f._data(this[0], "parsedAttrs")) {
                          e = this[0].attributes;
                          for (var i = 0, j = e.length; i < j; i++)
                            (g = e[i].name),
                              g.indexOf("data-") === 0 &&
                                ((g = f.camelCase(g.substring(5))), l(this[0], g, h[g]));
                          f._data(this[0], "parsedAttrs", !0);
                        }
                      }
                      return h;
                    }
                    if (typeof a == "object")
                      return this.each(function () {
                        f.data(this, a);
                      });
                    (d = a.split(".")), (d[1] = d[1] ? "." + d[1] : "");
                    if (c === b) {
                      (h = this.triggerHandler("getData" + d[1] + "!", [d[0]])),
                        h === b &&
                          this.length &&
                          ((h = f.data(this[0], a)), (h = l(this[0], a, h)));
                      return h === b && d[1] ? this.data(d[0]) : h;
                    }
                    return this.each(function () {
                      var b = f(this),
                        e = [d[0], c];
                      b.triggerHandler("setData" + d[1] + "!", e),
                        f.data(this, a, c),
                        b.triggerHandler("changeData" + d[1] + "!", e);
                    });
                  },
                  removeData: function (a) {
                    return this.each(function () {
                      f.removeData(this, a);
                    });
                  },
                }),
                f.extend({
                  _mark: function (a, b) {
                    a &&
                      ((b = (b || "fx") + "mark"), f._data(a, b, (f._data(a, b) || 0) + 1));
                  },
                  _unmark: function (a, b, c) {
                    a !== !0 && ((c = b), (b = a), (a = !1));
                    if (b) {
                      c = c || "fx";
                      var d = c + "mark",
                        e = a ? 0 : (f._data(b, d) || 1) - 1;
                      e ? f._data(b, d, e) : (f.removeData(b, d, !0), n(b, c, "mark"));
                    }
                  },
                  queue: function (a, b, c) {
                    var d;
                    if (a) {
                      (b = (b || "fx") + "queue"),
                        (d = f._data(a, b)),
                        c &&
                          (!d || f.isArray(c)
                            ? (d = f._data(a, b, f.makeArray(c)))
                            : d.push(c));
                      return d || [];
                    }
                  },
                  dequeue: function (a, b) {
                    b = b || "fx";
                    var c = f.queue(a, b),
                      d = c.shift(),
                      e = {};
                    d === "inprogress" && (d = c.shift()),
                      d &&
                        (b === "fx" && c.unshift("inprogress"),
                        f._data(a, b + ".run", e),
                        d.call(
                          a,
                          function () {
                            f.dequeue(a, b);
                          },
                          e
                        )),
                      c.length ||
                        (f.removeData(a, b + "queue " + b + ".run", !0), n(a, b, "queue"));
                  },
                }),
                f.fn.extend({
                  queue: function (a, c) {
                    typeof a != "string" && ((c = a), (a = "fx"));
                    if (c === b) return f.queue(this[0], a);
                    return this.each(function () {
                      var b = f.queue(this, a, c);
                      a === "fx" && b[0] !== "inprogress" && f.dequeue(this, a);
                    });
                  },
                  dequeue: function (a) {
                    return this.each(function () {
                      f.dequeue(this, a);
                    });
                  },
                  delay: function (a, b) {
                    (a = f.fx ? f.fx.speeds[a] || a : a), (b = b || "fx");
                    return this.queue(b, function (b, c) {
                      var d = setTimeout(b, a);
                      c.stop = function () {
                        clearTimeout(d);
                      };
                    });
                  },
                  clearQueue: function (a) {
                    return this.queue(a || "fx", []);
                  },
                  promise: function (a, c) {
                    function m() {
                      --h || d.resolveWith(e, [e]);
                    }
                    typeof a != "string" && ((c = a), (a = b)), (a = a || "fx");
                    var d = f.Deferred(),
                      e = this,
                      g = e.length,
                      h = 1,
                      i = a + "defer",
                      j = a + "queue",
                      k = a + "mark",
                      l;
                    while (g--)
                      if (
                        (l =
                          f.data(e[g], i, b, !0) ||
                          ((f.data(e[g], j, b, !0) || f.data(e[g], k, b, !0)) &&
                            f.data(e[g], i, f.Callbacks("once memory"), !0)))
                      )
                        h++, l.add(m);
                    m();
                    return d.promise();
                  },
                });
              var o = /[\n\t\r]/g,
                p = /\s+/,
                q = /\r/g,
                r = /^(?:button|input)$/i,
                s = /^(?:button|input|object|select|textarea)$/i,
                t = /^a(?:rea)?$/i,
                u =
                  /^(?:autofocus|autoplay|async|checked|controls|defer|disabled|hidden|loop|multiple|open|readonly|required|scoped|selected)$/i,
                v = f.support.getSetAttribute,
                w,
                x,
                y;
              f.fn.extend({
                attr: function (a, b) {
                  return f.access(this, a, b, !0, f.attr);
                },
                removeAttr: function (a) {
                  return this.each(function () {
                    f.removeAttr(this, a);
                  });
                },
                prop: function (a, b) {
                  return f.access(this, a, b, !0, f.prop);
                },
                removeProp: function (a) {
                  a = f.propFix[a] || a;
                  return this.each(function () {
                    try {
                      (this[a] = b), delete this[a];
                    } catch (c) {}
                  });
                },
                addClass: function (a) {
                  var b, c, d, e, g, h, i;
                  if (f.isFunction(a))
                    return this.each(function (b) {
                      f(this).addClass(a.call(this, b, this.className));
                    });
                  if (a && typeof a == "string") {
                    b = a.split(p);
                    for (c = 0, d = this.length; c < d; c++) {
                      e = this[c];
                      if (e.nodeType === 1)
                        if (!e.className && b.length === 1) e.className = a;
                        else {
                          g = " " + e.className + " ";
                          for (h = 0, i = b.length; h < i; h++)
                            ~g.indexOf(" " + b[h] + " ") || (g += b[h] + " ");
                          e.className = f.trim(g);
                        }
                    }
                  }
                  return this;
                },
                removeClass: function (a) {
                  var c, d, e, g, h, i, j;
                  if (f.isFunction(a))
                    return this.each(function (b) {
                      f(this).removeClass(a.call(this, b, this.className));
                    });
                  if ((a && typeof a == "string") || a === b) {
                    c = (a || "").split(p);
                    for (d = 0, e = this.length; d < e; d++) {
                      g = this[d];
                      if (g.nodeType === 1 && g.className)
                        if (a) {
                          h = (" " + g.className + " ").replace(o, " ");
                          for (i = 0, j = c.length; i < j; i++)
                            h = h.replace(" " + c[i] + " ", " ");
                          g.className = f.trim(h);
                        } else g.className = "";
                    }
                  }
                  return this;
                },
                toggleClass: function (a, b) {
                  var c = typeof a,
                    d = typeof b == "boolean";
                  if (f.isFunction(a))
                    return this.each(function (c) {
                      f(this).toggleClass(a.call(this, c, this.className, b), b);
                    });
                  return this.each(function () {
                    if (c === "string") {
                      var e,
                        g = 0,
                        h = f(this),
                        i = b,
                        j = a.split(p);
                      while ((e = j[g++]))
                        (i = d ? i : !h.hasClass(e)), h[i ? "addClass" : "removeClass"](e);
                    } else if (c === "undefined" || c === "boolean") this.className && f._data(this, "__className__", this.className), (this.className = this.className || a === !1 ? "" : f._data(this, "__className__") || "");
                  });
                },
                hasClass: function (a) {
                  var b = " " + a + " ",
                    c = 0,
                    d = this.length;
                  for (; c < d; c++)
                    if (
                      this[c].nodeType === 1 &&
                      (" " + this[c].className + " ").replace(o, " ").indexOf(b) > -1
                    )
                      return !0;
                  return !1;
                },
                val: function (a) {
                  var c,
                    d,
                    e,
                    g = this[0];
                  {
                    if (!!arguments.length) {
                      e = f.isFunction(a);
                      return this.each(function (d) {
                        var g = f(this),
                          h;
                        if (this.nodeType === 1) {
                          e ? (h = a.call(this, d, g.val())) : (h = a),
                            h == null
                              ? (h = "")
                              : typeof h == "number"
                              ? (h += "")
                              : f.isArray(h) &&
                                (h = f.map(h, function (a) {
                                  return a == null ? "" : a + "";
                                })),
                            (c =
                              f.valHooks[this.nodeName.toLowerCase()] ||
                              f.valHooks[this.type]);
                          if (!c || !("set" in c) || c.set(this, h, "value") === b)
                            this.value = h;
                        }
                      });
                    }
                    if (g) {
                      c = f.valHooks[g.nodeName.toLowerCase()] || f.valHooks[g.type];
                      if (c && "get" in c && (d = c.get(g, "value")) !== b) return d;
                      d = g.value;
                      return typeof d == "string" ? d.replace(q, "") : d == null ? "" : d;
                    }
                  }
                },
              }),
                f.extend({
                  valHooks: {
                    option: {
                      get: function (a) {
                        var b = a.attributes.value;
                        return !b || b.specified ? a.value : a.text;
                      },
                    },
                    select: {
                      get: function (a) {
                        var b,
                          c,
                          d,
                          e,
                          g = a.selectedIndex,
                          h = [],
                          i = a.options,
                          j = a.type === "select-one";
                        if (g < 0) return null;
                        (c = j ? g : 0), (d = j ? g + 1 : i.length);
                        for (; c < d; c++) {
                          e = i[c];
                          if (
                            e.selected &&
                            (f.support.optDisabled
                              ? !e.disabled
                              : e.getAttribute("disabled") === null) &&
                            (!e.parentNode.disabled ||
                              !f.nodeName(e.parentNode, "optgroup"))
                          ) {
                            b = f(e).val();
                            if (j) return b;
                            h.push(b);
                          }
                        }
                        if (j && !h.length && i.length) return f(i[g]).val();
                        return h;
                      },
                      set: function (a, b) {
                        var c = f.makeArray(b);
                        f(a)
                          .find("option")
                          .each(function () {
                            this.selected = f.inArray(f(this).val(), c) >= 0;
                          }),
                          c.length || (a.selectedIndex = -1);
                        return c;
                      },
                    },
                  },
                  attrFn: {
                    val: !0,
                    css: !0,
                    html: !0,
                    text: !0,
                    data: !0,
                    width: !0,
                    height: !0,
                    offset: !0,
                  },
                  attr: function (a, c, d, e) {
                    var g,
                      h,
                      i,
                      j = a.nodeType;
                    if (!!a && j !== 3 && j !== 8 && j !== 2) {
                      if (e && c in f.attrFn) return f(a)[c](d);
                      if (typeof a.getAttribute == "undefined") return f.prop(a, c, d);
                      (i = j !== 1 || !f.isXMLDoc(a)),
                        i &&
                          ((c = c.toLowerCase()),
                          (h = f.attrHooks[c] || (u.test(c) ? x : w)));
                      if (d !== b) {
                        if (d === null) {
                          f.removeAttr(a, c);
                          return;
                        }
                        if (h && "set" in h && i && (g = h.set(a, d, c)) !== b) return g;
                        a.setAttribute(c, "" + d);
                        return d;
                      }
                      if (h && "get" in h && i && (g = h.get(a, c)) !== null) return g;
                      g = a.getAttribute(c);
                      return g === null ? b : g;
                    }
                  },
                  removeAttr: function (a, b) {
                    var c,
                      d,
                      e,
                      g,
                      h = 0;
                    if (b && a.nodeType === 1) {
                      (d = b.toLowerCase().split(p)), (g = d.length);
                      for (; h < g; h++)
                        (e = d[h]),
                          e &&
                            ((c = f.propFix[e] || e),
                            f.attr(a, e, ""),
                            a.removeAttribute(v ? e : c),
                            u.test(e) && c in a && (a[c] = !1));
                    }
                  },
                  attrHooks: {
                    type: {
                      set: function (a, b) {
                        if (r.test(a.nodeName) && a.parentNode)
                          f.error("type property can't be changed");
                        else if (
                          !f.support.radioValue &&
                          b === "radio" &&
                          f.nodeName(a, "input")
                        ) {
                          var c = a.value;
                          a.setAttribute("type", b), c && (a.value = c);
                          return b;
                        }
                      },
                    },
                    value: {
                      get: function (a, b) {
                        if (w && f.nodeName(a, "button")) return w.get(a, b);
                        return b in a ? a.value : null;
                      },
                      set: function (a, b, c) {
                        if (w && f.nodeName(a, "button")) return w.set(a, b, c);
                        a.value = b;
                      },
                    },
                  },
                  propFix: {
                    tabindex: "tabIndex",
                    readonly: "readOnly",
                    for: "htmlFor",
                    class: "className",
                    maxlength: "maxLength",
                    cellspacing: "cellSpacing",
                    cellpadding: "cellPadding",
                    rowspan: "rowSpan",
                    colspan: "colSpan",
                    usemap: "useMap",
                    frameborder: "frameBorder",
                    contenteditable: "contentEditable",
                  },
                  prop: function (a, c, d) {
                    var e,
                      g,
                      h,
                      i = a.nodeType;
                    if (!!a && i !== 3 && i !== 8 && i !== 2) {
                      (h = i !== 1 || !f.isXMLDoc(a)),
                        h && ((c = f.propFix[c] || c), (g = f.propHooks[c]));
                      return d !== b
                        ? g && "set" in g && (e = g.set(a, d, c)) !== b
                          ? e
                          : (a[c] = d)
                        : g && "get" in g && (e = g.get(a, c)) !== null
                        ? e
                        : a[c];
                    }
                  },
                  propHooks: {
                    tabIndex: {
                      get: function (a) {
                        var c = a.getAttributeNode("tabindex");
                        return c && c.specified
                          ? parseInt(c.value, 10)
                          : s.test(a.nodeName) || (t.test(a.nodeName) && a.href)
                          ? 0
                          : b;
                      },
                    },
                  },
                }),
                (f.attrHooks.tabindex = f.propHooks.tabIndex),
                (x = {
                  get: function (a, c) {
                    var d,
                      e = f.prop(a, c);
                    return e === !0 ||
                      (typeof e != "boolean" &&
                        (d = a.getAttributeNode(c)) &&
                        d.nodeValue !== !1)
                      ? c.toLowerCase()
                      : b;
                  },
                  set: function (a, b, c) {
                    var d;
                    b === !1
                      ? f.removeAttr(a, c)
                      : ((d = f.propFix[c] || c),
                        d in a && (a[d] = !0),
                        a.setAttribute(c, c.toLowerCase()));
                    return c;
                  },
                }),
                v ||
                  ((y = { name: !0, id: !0 }),
                  (w = f.valHooks.button =
                    {
                      get: function (a, c) {
                        var d;
                        d = a.getAttributeNode(c);
                        return d && (y[c] ? d.nodeValue !== "" : d.specified)
                          ? d.nodeValue
                          : b;
                      },
                      set: function (a, b, d) {
                        var e = a.getAttributeNode(d);
                        e || ((e = c.createAttribute(d)), a.setAttributeNode(e));
                        return (e.nodeValue = b + "");
                      },
                    }),
                  (f.attrHooks.tabindex.set = w.set),
                  f.each(["width", "height"], function (a, b) {
                    f.attrHooks[b] = f.extend(f.attrHooks[b], {
                      set: function (a, c) {
                        if (c === "") {
                          a.setAttribute(b, "auto");
                          return c;
                        }
                      },
                    });
                  }),
                  (f.attrHooks.contenteditable = {
                    get: w.get,
                    set: function (a, b, c) {
                      b === "" && (b = "false"), w.set(a, b, c);
                    },
                  })),
                f.support.hrefNormalized ||
                  f.each(["href", "src", "width", "height"], function (a, c) {
                    f.attrHooks[c] = f.extend(f.attrHooks[c], {
                      get: function (a) {
                        var d = a.getAttribute(c, 2);
                        return d === null ? b : d;
                      },
                    });
                  }),
                f.support.style ||
                  (f.attrHooks.style = {
                    get: function (a) {
                      return a.style.cssText.toLowerCase() || b;
                    },
                    set: function (a, b) {
                      return (a.style.cssText = "" + b);
                    },
                  }),
                f.support.optSelected ||
                  (f.propHooks.selected = f.extend(f.propHooks.selected, {
                    get: function (a) {
                      var b = a.parentNode;
                      b && (b.selectedIndex, b.parentNode && b.parentNode.selectedIndex);
                      return null;
                    },
                  })),
                f.support.enctype || (f.propFix.enctype = "encoding"),
                f.support.checkOn ||
                  f.each(["radio", "checkbox"], function () {
                    f.valHooks[this] = {
                      get: function (a) {
                        return a.getAttribute("value") === null ? "on" : a.value;
                      },
                    };
                  }),
                f.each(["radio", "checkbox"], function () {
                  f.valHooks[this] = f.extend(f.valHooks[this], {
                    set: function (a, b) {
                      if (f.isArray(b)) return (a.checked = f.inArray(f(a).val(), b) >= 0);
                    },
                  });
                });
              var z = /^(?:textarea|input|select)$/i,
                A = /^([^\.]*)?(?:\.(.+))?$/,
                B = /\bhover(\.\S+)?\b/,
                C = /^key/,
                D = /^(?:mouse|contextmenu)|click/,
                E = /^(?:focusinfocus|focusoutblur)$/,
                F = /^(\w*)(?:#([\w\-]+))?(?:\.([\w\-]+))?$/,
                G = function (a) {
                  var b = F.exec(a);
                  b &&
                    ((b[1] = (b[1] || "").toLowerCase()),
                    (b[3] = b[3] && new RegExp("(?:^|\\s)" + b[3] + "(?:\\s|$)")));
                  return b;
                },
                H = function (a, b) {
                  var c = a.attributes || {};
                  return (
                    (!b[1] || a.nodeName.toLowerCase() === b[1]) &&
                    (!b[2] || (c.id || {}).value === b[2]) &&
                    (!b[3] || b[3].test((c["class"] || {}).value))
                  );
                },
                I = function (a) {
                  return f.event.special.hover
                    ? a
                    : a.replace(B, "mouseenter$1 mouseleave$1");
                };
              (f.event = {
                add: function (a, c, d, e, g) {
                  var h, i, j, k, l, m, n, o, p, q, r, s;
                  if (
                    !(a.nodeType === 3 || a.nodeType === 8 || !c || !d || !(h = f._data(a)))
                  ) {
                    d.handler && ((p = d), (d = p.handler)),
                      d.guid || (d.guid = f.guid++),
                      (j = h.events),
                      j || (h.events = j = {}),
                      (i = h.handle),
                      i ||
                        ((h.handle = i =
                          function (a) {
                            return typeof f != "undefined" &&
                              (!a || f.event.triggered !== a.type)
                              ? f.event.dispatch.apply(i.elem, arguments)
                              : b;
                          }),
                        (i.elem = a)),
                      (c = f.trim(I(c)).split(" "));
                    for (k = 0; k < c.length; k++) {
                      (l = A.exec(c[k]) || []),
                        (m = l[1]),
                        (n = (l[2] || "").split(".").sort()),
                        (s = f.event.special[m] || {}),
                        (m = (g ? s.delegateType : s.bindType) || m),
                        (s = f.event.special[m] || {}),
                        (o = f.extend(
                          {
                            type: m,
                            origType: l[1],
                            data: e,
                            handler: d,
                            guid: d.guid,
                            selector: g,
                            quick: G(g),
                            namespace: n.join("."),
                          },
                          p
                        )),
                        (r = j[m]);
                      if (!r) {
                        (r = j[m] = []), (r.delegateCount = 0);
                        if (!s.setup || s.setup.call(a, e, n, i) === !1)
                          a.addEventListener
                            ? a.addEventListener(m, i, !1)
                            : a.attachEvent && a.attachEvent("on" + m, i);
                      }
                      s.add &&
                        (s.add.call(a, o), o.handler.guid || (o.handler.guid = d.guid)),
                        g ? r.splice(r.delegateCount++, 0, o) : r.push(o),
                        (f.event.global[m] = !0);
                    }
                    a = null;
                  }
                },
                global: {},
                remove: function (a, b, c, d, e) {
                  var g = f.hasData(a) && f._data(a),
                    h,
                    i,
                    j,
                    k,
                    l,
                    m,
                    n,
                    o,
                    p,
                    q,
                    r,
                    s;
                  if (!!g && !!(o = g.events)) {
                    b = f.trim(I(b || "")).split(" ");
                    for (h = 0; h < b.length; h++) {
                      (i = A.exec(b[h]) || []), (j = k = i[1]), (l = i[2]);
                      if (!j) {
                        for (j in o) f.event.remove(a, j + b[h], c, d, !0);
                        continue;
                      }
                      (p = f.event.special[j] || {}),
                        (j = (d ? p.delegateType : p.bindType) || j),
                        (r = o[j] || []),
                        (m = r.length),
                        (l = l
                          ? new RegExp(
                              "(^|\\.)" +
                                l.split(".").sort().join("\\.(?:.*\\.)?") +
                                "(\\.|$)"
                            )
                          : null);
                      for (n = 0; n < r.length; n++)
                        (s = r[n]),
                          (e || k === s.origType) &&
                            (!c || c.guid === s.guid) &&
                            (!l || l.test(s.namespace)) &&
                            (!d || d === s.selector || (d === "**" && s.selector)) &&
                            (r.splice(n--, 1),
                            s.selector && r.delegateCount--,
                            p.remove && p.remove.call(a, s));
                      r.length === 0 &&
                        m !== r.length &&
                        ((!p.teardown || p.teardown.call(a, l) === !1) &&
                          f.removeEvent(a, j, g.handle),
                        delete o[j]);
                    }
                    f.isEmptyObject(o) &&
                      ((q = g.handle),
                      q && (q.elem = null),
                      f.removeData(a, ["events", "handle"], !0));
                  }
                },
                customEvent: { getData: !0, setData: !0, changeData: !0 },
                trigger: function (c, d, e, g) {
                  if (!e || (e.nodeType !== 3 && e.nodeType !== 8)) {
                    var h = c.type || c,
                      i = [],
                      j,
                      k,
                      l,
                      m,
                      n,
                      o,
                      p,
                      q,
                      r,
                      s;
                    if (E.test(h + f.event.triggered)) return;
                    h.indexOf("!") >= 0 && ((h = h.slice(0, -1)), (k = !0)),
                      h.indexOf(".") >= 0 &&
                        ((i = h.split(".")), (h = i.shift()), i.sort());
                    if ((!e || f.event.customEvent[h]) && !f.event.global[h]) return;
                    (c =
                      typeof c == "object"
                        ? c[f.expando]
                          ? c
                          : new f.Event(h, c)
                        : new f.Event(h)),
                      (c.type = h),
                      (c.isTrigger = !0),
                      (c.exclusive = k),
                      (c.namespace = i.join(".")),
                      (c.namespace_re = c.namespace
                        ? new RegExp("(^|\\.)" + i.join("\\.(?:.*\\.)?") + "(\\.|$)")
                        : null),
                      (o = h.indexOf(":") < 0 ? "on" + h : "");
                    if (!e) {
                      j = f.cache;
                      for (l in j)
                        j[l].events &&
                          j[l].events[h] &&
                          f.event.trigger(c, d, j[l].handle.elem, !0);
                      return;
                    }
                    (c.result = b),
                      c.target || (c.target = e),
                      (d = d != null ? f.makeArray(d) : []),
                      d.unshift(c),
                      (p = f.event.special[h] || {});
                    if (p.trigger && p.trigger.apply(e, d) === !1) return;
                    r = [[e, p.bindType || h]];
                    if (!g && !p.noBubble && !f.isWindow(e)) {
                      (s = p.delegateType || h),
                        (m = E.test(s + h) ? e : e.parentNode),
                        (n = null);
                      for (; m; m = m.parentNode) r.push([m, s]), (n = m);
                      n &&
                        n === e.ownerDocument &&
                        r.push([n.defaultView || n.parentWindow || a, s]);
                    }
                    for (l = 0; l < r.length && !c.isPropagationStopped(); l++)
                      (m = r[l][0]),
                        (c.type = r[l][1]),
                        (q = (f._data(m, "events") || {})[c.type] && f._data(m, "handle")),
                        q && q.apply(m, d),
                        (q = o && m[o]),
                        q && f.acceptData(m) && q.apply(m, d) === !1 && c.preventDefault();
                    (c.type = h),
                      !g &&
                        !c.isDefaultPrevented() &&
                        (!p._default || p._default.apply(e.ownerDocument, d) === !1) &&
                        (h !== "click" || !f.nodeName(e, "a")) &&
                        f.acceptData(e) &&
                        o &&
                        e[h] &&
                        ((h !== "focus" && h !== "blur") || c.target.offsetWidth !== 0) &&
                        !f.isWindow(e) &&
                        ((n = e[o]),
                        n && (e[o] = null),
                        (f.event.triggered = h),
                        e[h](),
                        (f.event.triggered = b),
                        n && (e[o] = n));
                    return c.result;
                  }
                },
                dispatch: function (c) {
                  c = f.event.fix(c || a.event);
                  var d = (f._data(this, "events") || {})[c.type] || [],
                    e = d.delegateCount,
                    g = [].slice.call(arguments, 0),
                    h = !c.exclusive && !c.namespace,
                    i = [],
                    j,
                    k,
                    l,
                    m,
                    n,
                    o,
                    p,
                    q,
                    r,
                    s,
                    t;
                  (g[0] = c), (c.delegateTarget = this);
                  if (e && !c.target.disabled && (!c.button || c.type !== "click")) {
                    (m = f(this)), (m.context = this.ownerDocument || this);
                    for (l = c.target; l != this; l = l.parentNode || this) {
                      (o = {}), (q = []), (m[0] = l);
                      for (j = 0; j < e; j++)
                        (r = d[j]),
                          (s = r.selector),
                          o[s] === b && (o[s] = r.quick ? H(l, r.quick) : m.is(s)),
                          o[s] && q.push(r);
                      q.length && i.push({ elem: l, matches: q });
                    }
                  }
                  d.length > e && i.push({ elem: this, matches: d.slice(e) });
                  for (j = 0; j < i.length && !c.isPropagationStopped(); j++) {
                    (p = i[j]), (c.currentTarget = p.elem);
                    for (
                      k = 0;
                      k < p.matches.length && !c.isImmediatePropagationStopped();
                      k++
                    ) {
                      r = p.matches[k];
                      if (
                        h ||
                        (!c.namespace && !r.namespace) ||
                        (c.namespace_re && c.namespace_re.test(r.namespace))
                      )
                        (c.data = r.data),
                          (c.handleObj = r),
                          (n = (
                            (f.event.special[r.origType] || {}).handle || r.handler
                          ).apply(p.elem, g)),
                          n !== b &&
                            ((c.result = n),
                            n === !1 && (c.preventDefault(), c.stopPropagation()));
                    }
                  }
                  return c.result;
                },
                props:
                  "attrChange attrName relatedNode srcElement altKey bubbles cancelable ctrlKey currentTarget eventPhase metaKey relatedTarget shiftKey target timeStamp view which".split(
                    " "
                  ),
                fixHooks: {},
                keyHooks: {
                  props: "char charCode key keyCode".split(" "),
                  filter: function (a, b) {
                    a.which == null &&
                      (a.which = b.charCode != null ? b.charCode : b.keyCode);
                    return a;
                  },
                },
                mouseHooks: {
                  props:
                    "button buttons clientX clientY fromElement offsetX offsetY pageX pageY screenX screenY toElement".split(
                      " "
                    ),
                  filter: function (a, d) {
                    var e,
                      f,
                      g,
                      h = d.button,
                      i = d.fromElement;
                    a.pageX == null &&
                      d.clientX != null &&
                      ((e = a.target.ownerDocument || c),
                      (f = e.documentElement),
                      (g = e.body),
                      (a.pageX =
                        d.clientX +
                        ((f && f.scrollLeft) || (g && g.scrollLeft) || 0) -
                        ((f && f.clientLeft) || (g && g.clientLeft) || 0)),
                      (a.pageY =
                        d.clientY +
                        ((f && f.scrollTop) || (g && g.scrollTop) || 0) -
                        ((f && f.clientTop) || (g && g.clientTop) || 0))),
                      !a.relatedTarget &&
                        i &&
                        (a.relatedTarget = i === a.target ? d.toElement : i),
                      !a.which &&
                        h !== b &&
                        (a.which = h & 1 ? 1 : h & 2 ? 3 : h & 4 ? 2 : 0);
                    return a;
                  },
                },
                fix: function (a) {
                  if (a[f.expando]) return a;
                  var d,
                    e,
                    g = a,
                    h = f.event.fixHooks[a.type] || {},
                    i = h.props ? this.props.concat(h.props) : this.props;
                  a = f.Event(g);
                  for (d = i.length; d; ) (e = i[--d]), (a[e] = g[e]);
                  a.target || (a.target = g.srcElement || c),
                    a.target.nodeType === 3 && (a.target = a.target.parentNode),
                    a.metaKey === b && (a.metaKey = a.ctrlKey);
                  return h.filter ? h.filter(a, g) : a;
                },
                special: {
                  ready: { setup: f.bindReady },
                  load: { noBubble: !0 },
                  focus: { delegateType: "focusin" },
                  blur: { delegateType: "focusout" },
                  beforeunload: {
                    setup: function (a, b, c) {
                      f.isWindow(this) && (this.onbeforeunload = c);
                    },
                    teardown: function (a, b) {
                      this.onbeforeunload === b && (this.onbeforeunload = null);
                    },
                  },
                },
                simulate: function (a, b, c, d) {
                  var e = f.extend(new f.Event(), c, {
                    type: a,
                    isSimulated: !0,
                    originalEvent: {},
                  });
                  d ? f.event.trigger(e, null, b) : f.event.dispatch.call(b, e),
                    e.isDefaultPrevented() && c.preventDefault();
                },
              }),
                (f.event.handle = f.event.dispatch),
                (f.removeEvent = c.removeEventListener
                  ? function (a, b, c) {
                      a.removeEventListener && a.removeEventListener(b, c, !1);
                    }
                  : function (a, b, c) {
                      a.detachEvent && a.detachEvent("on" + b, c);
                    }),
                (f.Event = function (a, b) {
                  if (!(this instanceof f.Event)) return new f.Event(a, b);
                  a && a.type
                    ? ((this.originalEvent = a),
                      (this.type = a.type),
                      (this.isDefaultPrevented =
                        a.defaultPrevented ||
                        a.returnValue === !1 ||
                        (a.getPreventDefault && a.getPreventDefault())
                          ? K
                          : J))
                    : (this.type = a),
                    b && f.extend(this, b),
                    (this.timeStamp = (a && a.timeStamp) || f.now()),
                    (this[f.expando] = !0);
                }),
                (f.Event.prototype = {
                  preventDefault: function () {
                    this.isDefaultPrevented = K;
                    var a = this.originalEvent;
                    !a || (a.preventDefault ? a.preventDefault() : (a.returnValue = !1));
                  },
                  stopPropagation: function () {
                    this.isPropagationStopped = K;
                    var a = this.originalEvent;
                    !a || (a.stopPropagation && a.stopPropagation(), (a.cancelBubble = !0));
                  },
                  stopImmediatePropagation: function () {
                    (this.isImmediatePropagationStopped = K), this.stopPropagation();
                  },
                  isDefaultPrevented: J,
                  isPropagationStopped: J,
                  isImmediatePropagationStopped: J,
                }),
                f.each(
                  { mouseenter: "mouseover", mouseleave: "mouseout" },
                  function (a, b) {
                    f.event.special[a] = {
                      delegateType: b,
                      bindType: b,
                      handle: function (a) {
                        var c = this,
                          d = a.relatedTarget,
                          e = a.handleObj,
                          g = e.selector,
                          h;
                        if (!d || (d !== c && !f.contains(c, d)))
                          (a.type = e.origType),
                            (h = e.handler.apply(this, arguments)),
                            (a.type = b);
                        return h;
                      },
                    };
                  }
                ),
                f.support.submitBubbles ||
                  (f.event.special.submit = {
                    setup: function () {
                      if (f.nodeName(this, "form")) return !1;
                      f.event.add(this, "click._submit keypress._submit", function (a) {
                        var c = a.target,
                          d =
                            f.nodeName(c, "input") || f.nodeName(c, "button") ? c.form : b;
                        d &&
                          !d._submit_attached &&
                          (f.event.add(d, "submit._submit", function (a) {
                            this.parentNode &&
                              !a.isTrigger &&
                              f.event.simulate("submit", this.parentNode, a, !0);
                          }),
                          (d._submit_attached = !0));
                      });
                    },
                    teardown: function () {
                      if (f.nodeName(this, "form")) return !1;
                      f.event.remove(this, "._submit");
                    },
                  }),
                f.support.changeBubbles ||
                  (f.event.special.change = {
                    setup: function () {
                      if (z.test(this.nodeName)) {
                        if (this.type === "checkbox" || this.type === "radio")
                          f.event.add(this, "propertychange._change", function (a) {
                            a.originalEvent.propertyName === "checked" &&
                              (this._just_changed = !0);
                          }),
                            f.event.add(this, "click._change", function (a) {
                              this._just_changed &&
                                !a.isTrigger &&
                                ((this._just_changed = !1),
                                f.event.simulate("change", this, a, !0));
                            });
                        return !1;
                      }
                      f.event.add(this, "beforeactivate._change", function (a) {
                        var b = a.target;
                        z.test(b.nodeName) &&
                          !b._change_attached &&
                          (f.event.add(b, "change._change", function (a) {
                            this.parentNode &&
                              !a.isSimulated &&
                              !a.isTrigger &&
                              f.event.simulate("change", this.parentNode, a, !0);
                          }),
                          (b._change_attached = !0));
                      });
                    },
                    handle: function (a) {
                      var b = a.target;
                      if (
                        this !== b ||
                        a.isSimulated ||
                        a.isTrigger ||
                        (b.type !== "radio" && b.type !== "checkbox")
                      )
                        return a.handleObj.handler.apply(this, arguments);
                    },
                    teardown: function () {
                      f.event.remove(this, "._change");
                      return z.test(this.nodeName);
                    },
                  }),
                f.support.focusinBubbles ||
                  f.each({ focus: "focusin", blur: "focusout" }, function (a, b) {
                    var d = 0,
                      e = function (a) {
                        f.event.simulate(b, a.target, f.event.fix(a), !0);
                      };
                    f.event.special[b] = {
                      setup: function () {
                        d++ === 0 && c.addEventListener(a, e, !0);
                      },
                      teardown: function () {
                        --d === 0 && c.removeEventListener(a, e, !0);
                      },
                    };
                  }),
                f.fn.extend({
                  on: function (a, c, d, e, g) {
                    var h, i;
                    if (typeof a == "object") {
                      typeof c != "string" && ((d = c), (c = b));
                      for (i in a) this.on(i, c, d, a[i], g);
                      return this;
                    }
                    d == null && e == null
                      ? ((e = c), (d = c = b))
                      : e == null &&
                        (typeof c == "string"
                          ? ((e = d), (d = b))
                          : ((e = d), (d = c), (c = b)));
                    if (e === !1) e = J;
                    else if (!e) return this;
                    g === 1 &&
                      ((h = e),
                      (e = function (a) {
                        f().off(a);
                        return h.apply(this, arguments);
                      }),
                      (e.guid = h.guid || (h.guid = f.guid++)));
                    return this.each(function () {
                      f.event.add(this, a, e, d, c);
                    });
                  },
                  one: function (a, b, c, d) {
                    return this.on.call(this, a, b, c, d, 1);
                  },
                  off: function (a, c, d) {
                    if (a && a.preventDefault && a.handleObj) {
                      var e = a.handleObj;
                      f(a.delegateTarget).off(
                        e.namespace ? e.type + "." + e.namespace : e.type,
                        e.selector,
                        e.handler
                      );
                      return this;
                    }
                    if (typeof a == "object") {
                      for (var g in a) this.off(g, c, a[g]);
                      return this;
                    }
                    if (c === !1 || typeof c == "function") (d = c), (c = b);
                    d === !1 && (d = J);
                    return this.each(function () {
                      f.event.remove(this, a, d, c);
                    });
                  },
                  bind: function (a, b, c) {
                    return this.on(a, null, b, c);
                  },
                  unbind: function (a, b) {
                    return this.off(a, null, b);
                  },
                  live: function (a, b, c) {
                    f(this.context).on(a, this.selector, b, c);
                    return this;
                  },
                  die: function (a, b) {
                    f(this.context).off(a, this.selector || "**", b);
                    return this;
                  },
                  delegate: function (a, b, c, d) {
                    return this.on(b, a, c, d);
                  },
                  undelegate: function (a, b, c) {
                    return arguments.length == 1 ? this.off(a, "**") : this.off(b, a, c);
                  },
                  trigger: function (a, b) {
                    return this.each(function () {
                      f.event.trigger(a, b, this);
                    });
                  },
                  triggerHandler: function (a, b) {
                    if (this[0]) return f.event.trigger(a, b, this[0], !0);
                  },
                  toggle: function (a) {
                    var b = arguments,
                      c = a.guid || f.guid++,
                      d = 0,
                      e = function (c) {
                        var e = (f._data(this, "lastToggle" + a.guid) || 0) % d;
                        f._data(this, "lastToggle" + a.guid, e + 1), c.preventDefault();
                        return b[e].apply(this, arguments) || !1;
                      };
                    e.guid = c;
                    while (d < b.length) b[d++].guid = c;
                    return this.click(e);
                  },
                  hover: function (a, b) {
                    return this.mouseenter(a).mouseleave(b || a);
                  },
                }),
                f.each(
                  "blur focus focusin focusout load resize scroll unload click dblclick mousedown mouseup mousemove mouseover mouseout mouseenter mouseleave change select submit keydown keypress keyup error contextmenu".split(
                    " "
                  ),
                  function (a, b) {
                    (f.fn[b] = function (a, c) {
                      c == null && ((c = a), (a = null));
                      return arguments.length > 0
                        ? this.on(b, null, a, c)
                        : this.trigger(b);
                    }),
                      f.attrFn && (f.attrFn[b] = !0),
                      C.test(b) && (f.event.fixHooks[b] = f.event.keyHooks),
                      D.test(b) && (f.event.fixHooks[b] = f.event.mouseHooks);
                  }
                ),
                (function () {
                  function x(a, b, c, e, f, g) {
                    for (var h = 0, i = e.length; h < i; h++) {
                      var j = e[h];
                      if (j) {
                        var k = !1;
                        j = j[a];
                        while (j) {
                          if (j[d] === c) {
                            k = e[j.sizset];
                            break;
                          }
                          if (j.nodeType === 1) {
                            g || ((j[d] = c), (j.sizset = h));
                            if (typeof b != "string") {
                              if (j === b) {
                                k = !0;
                                break;
                              }
                            } else if (m.filter(b, [j]).length > 0) {
                              k = j;
                              break;
                            }
                          }
                          j = j[a];
                        }
                        e[h] = k;
                      }
                    }
                  }
                  function w(a, b, c, e, f, g) {
                    for (var h = 0, i = e.length; h < i; h++) {
                      var j = e[h];
                      if (j) {
                        var k = !1;
                        j = j[a];
                        while (j) {
                          if (j[d] === c) {
                            k = e[j.sizset];
                            break;
                          }
                          j.nodeType === 1 && !g && ((j[d] = c), (j.sizset = h));
                          if (j.nodeName.toLowerCase() === b) {
                            k = j;
                            break;
                          }
                          j = j[a];
                        }
                        e[h] = k;
                      }
                    }
                  }
                  var a =
                      /((?:\((?:\([^()]+\)|[^()]+)+\)|\[(?:\[[^\[\]]*\]|['"][^'"]*['"]|[^\[\]'"]+)+\]|\\.|[^ >+~,(\[\\]+)+|[>+~])(\s*,\s*)?((?:.|\r|\n)*)/g,
                    d = "sizcache" + (Math.random() + "").replace(".", ""),
                    e = 0,
                    g = Object.prototype.toString,
                    h = !1,
                    i = !0,
                    j = /\\/g,
                    k = /\r\n/g,
                    l = /\W/;
                  [0, 0].sort(function () {
                    i = !1;
                    return 0;
                  });
                  var m = function (b, d, e, f) {
                    (e = e || []), (d = d || c);
                    var h = d;
                    if (d.nodeType !== 1 && d.nodeType !== 9) return [];
                    if (!b || typeof b != "string") return e;
                    var i,
                      j,
                      k,
                      l,
                      n,
                      q,
                      r,
                      t,
                      u = !0,
                      v = m.isXML(d),
                      w = [],
                      x = b;
                    do {
                      a.exec(""), (i = a.exec(x));
                      if (i) {
                        (x = i[3]), w.push(i[1]);
                        if (i[2]) {
                          l = i[3];
                          break;
                        }
                      }
                    } while (i);
                    if (w.length > 1 && p.exec(b))
                      if (w.length === 2 && o.relative[w[0]]) j = y(w[0] + w[1], d, f);
                      else {
                        j = o.relative[w[0]] ? [d] : m(w.shift(), d);
                        while (w.length)
                          (b = w.shift()),
                            o.relative[b] && (b += w.shift()),
                            (j = y(b, j, f));
                      }
                    else {
                      !f &&
                        w.length > 1 &&
                        d.nodeType === 9 &&
                        !v &&
                        o.match.ID.test(w[0]) &&
                        !o.match.ID.test(w[w.length - 1]) &&
                        ((n = m.find(w.shift(), d, v)),
                        (d = n.expr ? m.filter(n.expr, n.set)[0] : n.set[0]));
                      if (d) {
                        (n = f
                          ? { expr: w.pop(), set: s(f) }
                          : m.find(
                              w.pop(),
                              w.length === 1 &&
                                (w[0] === "~" || w[0] === "+") &&
                                d.parentNode
                                ? d.parentNode
                                : d,
                              v
                            )),
                          (j = n.expr ? m.filter(n.expr, n.set) : n.set),
                          w.length > 0 ? (k = s(j)) : (u = !1);
                        while (w.length)
                          (q = w.pop()),
                            (r = q),
                            o.relative[q] ? (r = w.pop()) : (q = ""),
                            r == null && (r = d),
                            o.relative[q](k, r, v);
                      } else k = w = [];
                    }
                    k || (k = j), k || m.error(q || b);
                    if (g.call(k) === "[object Array]")
                      if (!u) e.push.apply(e, k);
                      else if (d && d.nodeType === 1)
                        for (t = 0; k[t] != null; t++)
                          k[t] &&
                            (k[t] === !0 || (k[t].nodeType === 1 && m.contains(d, k[t]))) &&
                            e.push(j[t]);
                      else
                        for (t = 0; k[t] != null; t++)
                          k[t] && k[t].nodeType === 1 && e.push(j[t]);
                    else s(k, e);
                    l && (m(l, h, e, f), m.uniqueSort(e));
                    return e;
                  };
                  (m.uniqueSort = function (a) {
                    if (u) {
                      (h = i), a.sort(u);
                      if (h)
                        for (var b = 1; b < a.length; b++)
                          a[b] === a[b - 1] && a.splice(b--, 1);
                    }
                    return a;
                  }),
                    (m.matches = function (a, b) {
                      return m(a, null, null, b);
                    }),
                    (m.matchesSelector = function (a, b) {
                      return m(b, null, null, [a]).length > 0;
                    }),
                    (m.find = function (a, b, c) {
                      var d, e, f, g, h, i;
                      if (!a) return [];
                      for (e = 0, f = o.order.length; e < f; e++) {
                        h = o.order[e];
                        if ((g = o.leftMatch[h].exec(a))) {
                          (i = g[1]), g.splice(1, 1);
                          if (i.substr(i.length - 1) !== "\\") {
                            (g[1] = (g[1] || "").replace(j, "")), (d = o.find[h](g, b, c));
                            if (d != null) {
                              a = a.replace(o.match[h], "");
                              break;
                            }
                          }
                        }
                      }
                      d ||
                        (d =
                          typeof b.getElementsByTagName != "undefined"
                            ? b.getElementsByTagName("*")
                            : []);
                      return { set: d, expr: a };
                    }),
                    (m.filter = function (a, c, d, e) {
                      var f,
                        g,
                        h,
                        i,
                        j,
                        k,
                        l,
                        n,
                        p,
                        q = a,
                        r = [],
                        s = c,
                        t = c && c[0] && m.isXML(c[0]);
                      while (a && c.length) {
                        for (h in o.filter)
                          if ((f = o.leftMatch[h].exec(a)) != null && f[2]) {
                            (k = o.filter[h]), (l = f[1]), (g = !1), f.splice(1, 1);
                            if (l.substr(l.length - 1) === "\\") continue;
                            s === r && (r = []);
                            if (o.preFilter[h]) {
                              f = o.preFilter[h](f, s, d, r, e, t);
                              if (!f) g = i = !0;
                              else if (f === !0) continue;
                            }
                            if (f)
                              for (n = 0; (j = s[n]) != null; n++)
                                j &&
                                  ((i = k(j, f, n, s)),
                                  (p = e ^ i),
                                  d && i != null
                                    ? p
                                      ? (g = !0)
                                      : (s[n] = !1)
                                    : p && (r.push(j), (g = !0)));
                            if (i !== b) {
                              d || (s = r), (a = a.replace(o.match[h], ""));
                              if (!g) return [];
                              break;
                            }
                          }
                        if (a === q)
                          if (g == null) m.error(a);
                          else break;
                        q = a;
                      }
                      return s;
                    }),
                    (m.error = function (a) {
                      throw new Error("Syntax error, unrecognized expression: " + a);
                    });
                  var n = (m.getText = function (a) {
                      var b,
                        c,
                        d = a.nodeType,
                        e = "";
                      if (d) {
                        if (d === 1 || d === 9) {
                          if (typeof a.textContent == "string") return a.textContent;
                          if (typeof a.innerText == "string")
                            return a.innerText.replace(k, "");
                          for (a = a.firstChild; a; a = a.nextSibling) e += n(a);
                        } else if (d === 3 || d === 4) return a.nodeValue;
                      } else for (b = 0; (c = a[b]); b++) c.nodeType !== 8 && (e += n(c));
                      return e;
                    }),
                    o = (m.selectors = {
                      order: ["ID", "NAME", "TAG"],
                      match: {
                        ID: /#((?:[\w\u00c0-\uFFFF\-]|\\.)+)/,
                        CLASS: /\.((?:[\w\u00c0-\uFFFF\-]|\\.)+)/,
                        NAME: /\[name=['"]*((?:[\w\u00c0-\uFFFF\-]|\\.)+)['"]*\]/,
                        ATTR: /\[\s*((?:[\w\u00c0-\uFFFF\-]|\\.)+)\s*(?:(\S?=)\s*(?:(['"])(.*?)\3|(#?(?:[\w\u00c0-\uFFFF\-]|\\.)*)|)|)\s*\]/,
                        TAG: /^((?:[\w\u00c0-\uFFFF\*\-]|\\.)+)/,
                        CHILD:
                          /:(only|nth|last|first)-child(?:\(\s*(even|odd|(?:[+\-]?\d+|(?:[+\-]?\d*)?n\s*(?:[+\-]\s*\d+)?))\s*\))?/,
                        POS: /:(nth|eq|gt|lt|first|last|even|odd)(?:\((\d*)\))?(?=[^\-]|$)/,
                        PSEUDO:
                          /:((?:[\w\u00c0-\uFFFF\-]|\\.)+)(?:\((['"]?)((?:\([^\)]+\)|[^\(\)]*)+)\2\))?/,
                      },
                      leftMatch: {},
                      attrMap: { class: "className", for: "htmlFor" },
                      attrHandle: {
                        href: function (a) {
                          return a.getAttribute("href");
                        },
                        type: function (a) {
                          return a.getAttribute("type");
                        },
                      },
                      relative: {
                        "+": function (a, b) {
                          var c = typeof b == "string",
                            d = c && !l.test(b),
                            e = c && !d;
                          d && (b = b.toLowerCase());
                          for (var f = 0, g = a.length, h; f < g; f++)
                            if ((h = a[f])) {
                              while ((h = h.previousSibling) && h.nodeType !== 1);
                              a[f] =
                                e || (h && h.nodeName.toLowerCase() === b)
                                  ? h || !1
                                  : h === b;
                            }
                          e && m.filter(b, a, !0);
                        },
                        ">": function (a, b) {
                          var c,
                            d = typeof b == "string",
                            e = 0,
                            f = a.length;
                          if (d && !l.test(b)) {
                            b = b.toLowerCase();
                            for (; e < f; e++) {
                              c = a[e];
                              if (c) {
                                var g = c.parentNode;
                                a[e] = g.nodeName.toLowerCase() === b ? g : !1;
                              }
                            }
                          } else {
                            for (; e < f; e++)
                              (c = a[e]),
                                c && (a[e] = d ? c.parentNode : c.parentNode === b);
                            d && m.filter(b, a, !0);
                          }
                        },
                        "": function (a, b, c) {
                          var d,
                            f = e++,
                            g = x;
                          typeof b == "string" &&
                            !l.test(b) &&
                            ((b = b.toLowerCase()), (d = b), (g = w)),
                            g("parentNode", b, f, a, d, c);
                        },
                        "~": function (a, b, c) {
                          var d,
                            f = e++,
                            g = x;
                          typeof b == "string" &&
                            !l.test(b) &&
                            ((b = b.toLowerCase()), (d = b), (g = w)),
                            g("previousSibling", b, f, a, d, c);
                        },
                      },
                      find: {
                        ID: function (a, b, c) {
                          if (typeof b.getElementById != "undefined" && !c) {
                            var d = b.getElementById(a[1]);
                            return d && d.parentNode ? [d] : [];
                          }
                        },
                        NAME: function (a, b) {
                          if (typeof b.getElementsByName != "undefined") {
                            var c = [],
                              d = b.getElementsByName(a[1]);
                            for (var e = 0, f = d.length; e < f; e++)
                              d[e].getAttribute("name") === a[1] && c.push(d[e]);
                            return c.length === 0 ? null : c;
                          }
                        },
                        TAG: function (a, b) {
                          if (typeof b.getElementsByTagName != "undefined")
                            return b.getElementsByTagName(a[1]);
                        },
                      },
                      preFilter: {
                        CLASS: function (a, b, c, d, e, f) {
                          a = " " + a[1].replace(j, "") + " ";
                          if (f) return a;
                          for (var g = 0, h; (h = b[g]) != null; g++)
                            h &&
                              (e ^
                              (h.className &&
                                (" " + h.className + " ")
                                  .replace(/[\t\n\r]/g, " ")
                                  .indexOf(a) >= 0)
                                ? c || d.push(h)
                                : c && (b[g] = !1));
                          return !1;
                        },
                        ID: function (a) {
                          return a[1].replace(j, "");
                        },
                        TAG: function (a, b) {
                          return a[1].replace(j, "").toLowerCase();
                        },
                        CHILD: function (a) {
                          if (a[1] === "nth") {
                            a[2] || m.error(a[0]), (a[2] = a[2].replace(/^\+|\s*/g, ""));
                            var b = /(-?)(\d*)(?:n([+\-]?\d*))?/.exec(
                              (a[2] === "even" && "2n") ||
                                (a[2] === "odd" && "2n+1") ||
                                (!/\D/.test(a[2]) && "0n+" + a[2]) ||
                                a[2]
                            );
                            (a[2] = b[1] + (b[2] || 1) - 0), (a[3] = b[3] - 0);
                          } else a[2] && m.error(a[0]);
                          a[0] = e++;
                          return a;
                        },
                        ATTR: function (a, b, c, d, e, f) {
                          var g = (a[1] = a[1].replace(j, ""));
                          !f && o.attrMap[g] && (a[1] = o.attrMap[g]),
                            (a[4] = (a[4] || a[5] || "").replace(j, "")),
                            a[2] === "~=" && (a[4] = " " + a[4] + " ");
                          return a;
                        },
                        PSEUDO: function (b, c, d, e, f) {
                          if (b[1] === "not")
                            if ((a.exec(b[3]) || "").length > 1 || /^\w/.test(b[3]))
                              b[3] = m(b[3], null, null, c);
                            else {
                              var g = m.filter(b[3], c, d, !0 ^ f);
                              d || e.push.apply(e, g);
                              return !1;
                            }
                          else if (o.match.POS.test(b[0]) || o.match.CHILD.test(b[0]))
                            return !0;
                          return b;
                        },
                        POS: function (a) {
                          a.unshift(!0);
                          return a;
                        },
                      },
                      filters: {
                        enabled: function (a) {
                          return a.disabled === !1 && a.type !== "hidden";
                        },
                        disabled: function (a) {
                          return a.disabled === !0;
                        },
                        checked: function (a) {
                          return a.checked === !0;
                        },
                        selected: function (a) {
                          a.parentNode && a.parentNode.selectedIndex;
                          return a.selected === !0;
                        },
                        parent: function (a) {
                          return !!a.firstChild;
                        },
                        empty: function (a) {
                          return !a.firstChild;
                        },
                        has: function (a, b, c) {
                          return !!m(c[3], a).length;
                        },
                        header: function (a) {
                          return /h\d/i.test(a.nodeName);
                        },
                        text: function (a) {
                          var b = a.getAttribute("type"),
                            c = a.type;
                          return (
                            a.nodeName.toLowerCase() === "input" &&
                            "text" === c &&
                            (b === c || b === null)
                          );
                        },
                        radio: function (a) {
                          return a.nodeName.toLowerCase() === "input" && "radio" === a.type;
                        },
                        checkbox: function (a) {
                          return (
                            a.nodeName.toLowerCase() === "input" && "checkbox" === a.type
                          );
                        },
                        file: function (a) {
                          return a.nodeName.toLowerCase() === "input" && "file" === a.type;
                        },
                        password: function (a) {
                          return (
                            a.nodeName.toLowerCase() === "input" && "password" === a.type
                          );
                        },
                        submit: function (a) {
                          var b = a.nodeName.toLowerCase();
                          return (b === "input" || b === "button") && "submit" === a.type;
                        },
                        image: function (a) {
                          return a.nodeName.toLowerCase() === "input" && "image" === a.type;
                        },
                        reset: function (a) {
                          var b = a.nodeName.toLowerCase();
                          return (b === "input" || b === "button") && "reset" === a.type;
                        },
                        button: function (a) {
                          var b = a.nodeName.toLowerCase();
                          return (b === "input" && "button" === a.type) || b === "button";
                        },
                        input: function (a) {
                          return /input|select|textarea|button/i.test(a.nodeName);
                        },
                        focus: function (a) {
                          return a === a.ownerDocument.activeElement;
                        },
                      },
                      setFilters: {
                        first: function (a, b) {
                          return b === 0;
                        },
                        last: function (a, b, c, d) {
                          return b === d.length - 1;
                        },
                        even: function (a, b) {
                          return b % 2 === 0;
                        },
                        odd: function (a, b) {
                          return b % 2 === 1;
                        },
                        lt: function (a, b, c) {
                          return b < c[3] - 0;
                        },
                        gt: function (a, b, c) {
                          return b > c[3] - 0;
                        },
                        nth: function (a, b, c) {
                          return c[3] - 0 === b;
                        },
                        eq: function (a, b, c) {
                          return c[3] - 0 === b;
                        },
                      },
                      filter: {
                        PSEUDO: function (a, b, c, d) {
                          var e = b[1],
                            f = o.filters[e];
                          if (f) return f(a, c, b, d);
                          if (e === "contains")
                            return (
                              (a.textContent || a.innerText || n([a]) || "").indexOf(
                                b[3]
                              ) >= 0
                            );
                          if (e === "not") {
                            var g = b[3];
                            for (var h = 0, i = g.length; h < i; h++)
                              if (g[h] === a) return !1;
                            return !0;
                          }
                          m.error(e);
                        },
                        CHILD: function (a, b) {
                          var c,
                            e,
                            f,
                            g,
                            h,
                            i,
                            j,
                            k = b[1],
                            l = a;
                          switch (k) {
                            case "only":
                            case "first":
                              while ((l = l.previousSibling))
                                if (l.nodeType === 1) return !1;
                              if (k === "first") return !0;
                              l = a;
                            case "last":
                              while ((l = l.nextSibling)) if (l.nodeType === 1) return !1;
                              return !0;
                            case "nth":
                              (c = b[2]), (e = b[3]);
                              if (c === 1 && e === 0) return !0;
                              (f = b[0]), (g = a.parentNode);
                              if (g && (g[d] !== f || !a.nodeIndex)) {
                                i = 0;
                                for (l = g.firstChild; l; l = l.nextSibling)
                                  l.nodeType === 1 && (l.nodeIndex = ++i);
                                g[d] = f;
                              }
                              j = a.nodeIndex - e;
                              return c === 0 ? j === 0 : j % c === 0 && j / c >= 0;
                          }
                        },
                        ID: function (a, b) {
                          return a.nodeType === 1 && a.getAttribute("id") === b;
                        },
                        TAG: function (a, b) {
                          return (
                            (b === "*" && a.nodeType === 1) ||
                            (!!a.nodeName && a.nodeName.toLowerCase() === b)
                          );
                        },
                        CLASS: function (a, b) {
                          return (
                            (" " + (a.className || a.getAttribute("class")) + " ").indexOf(
                              b
                            ) > -1
                          );
                        },
                        ATTR: function (a, b) {
                          var c = b[1],
                            d = m.attr
                              ? m.attr(a, c)
                              : o.attrHandle[c]
                              ? o.attrHandle[c](a)
                              : a[c] != null
                              ? a[c]
                              : a.getAttribute(c),
                            e = d + "",
                            f = b[2],
                            g = b[4];
                          return d == null
                            ? f === "!="
                            : !f && m.attr
                            ? d != null
                            : f === "="
                            ? e === g
                            : f === "*="
                            ? e.indexOf(g) >= 0
                            : f === "~="
                            ? (" " + e + " ").indexOf(g) >= 0
                            : g
                            ? f === "!="
                              ? e !== g
                              : f === "^="
                              ? e.indexOf(g) === 0
                              : f === "$="
                              ? e.substr(e.length - g.length) === g
                              : f === "|="
                              ? e === g || e.substr(0, g.length + 1) === g + "-"
                              : !1
                            : e && d !== !1;
                        },
                        POS: function (a, b, c, d) {
                          var e = b[2],
                            f = o.setFilters[e];
                          if (f) return f(a, c, b, d);
                        },
                      },
                    }),
                    p = o.match.POS,
                    q = function (a, b) {
                      return "\\" + (b - 0 + 1);
                    };
                  for (var r in o.match)
                    (o.match[r] = new RegExp(
                      o.match[r].source + /(?![^\[]*\])(?![^\(]*\))/.source
                    )),
                      (o.leftMatch[r] = new RegExp(
                        /(^(?:.|\r|\n)*?)/.source + o.match[r].source.replace(/\\(\d+)/g, q)
                      ));
                  var s = function (a, b) {
                    a = Array.prototype.slice.call(a, 0);
                    if (b) {
                      b.push.apply(b, a);
                      return b;
                    }
                    return a;
                  };
                  try {
                    Array.prototype.slice.call(c.documentElement.childNodes, 0)[0].nodeType;
                  } catch (t) {
                    s = function (a, b) {
                      var c = 0,
                        d = b || [];
                      if (g.call(a) === "[object Array]") Array.prototype.push.apply(d, a);
                      else if (typeof a.length == "number")
                        for (var e = a.length; c < e; c++) d.push(a[c]);
                      else for (; a[c]; c++) d.push(a[c]);
                      return d;
                    };
                  }
                  var u, v;
                  c.documentElement.compareDocumentPosition
                    ? (u = function (a, b) {
                        if (a === b) {
                          h = !0;
                          return 0;
                        }
                        if (!a.compareDocumentPosition || !b.compareDocumentPosition)
                          return a.compareDocumentPosition ? -1 : 1;
                        return a.compareDocumentPosition(b) & 4 ? -1 : 1;
                      })
                    : ((u = function (a, b) {
                        if (a === b) {
                          h = !0;
                          return 0;
                        }
                        if (a.sourceIndex && b.sourceIndex)
                          return a.sourceIndex - b.sourceIndex;
                        var c,
                          d,
                          e = [],
                          f = [],
                          g = a.parentNode,
                          i = b.parentNode,
                          j = g;
                        if (g === i) return v(a, b);
                        if (!g) return -1;
                        if (!i) return 1;
                        while (j) e.unshift(j), (j = j.parentNode);
                        j = i;
                        while (j) f.unshift(j), (j = j.parentNode);
                        (c = e.length), (d = f.length);
                        for (var k = 0; k < c && k < d; k++)
                          if (e[k] !== f[k]) return v(e[k], f[k]);
                        return k === c ? v(a, f[k], -1) : v(e[k], b, 1);
                      }),
                      (v = function (a, b, c) {
                        if (a === b) return c;
                        var d = a.nextSibling;
                        while (d) {
                          if (d === b) return -1;
                          d = d.nextSibling;
                        }
                        return 1;
                      })),
                    (function () {
                      var a = c.createElement("div"),
                        d = "script" + new Date().getTime(),
                        e = c.documentElement;
                      (a.innerHTML = "<a name='" + d + "'/>"),
                        e.insertBefore(a, e.firstChild),
                        c.getElementById(d) &&
                          ((o.find.ID = function (a, c, d) {
                            if (typeof c.getElementById != "undefined" && !d) {
                              var e = c.getElementById(a[1]);
                              return e
                                ? e.id === a[1] ||
                                  (typeof e.getAttributeNode != "undefined" &&
                                    e.getAttributeNode("id").nodeValue === a[1])
                                  ? [e]
                                  : b
                                : [];
                            }
                          }),
                          (o.filter.ID = function (a, b) {
                            var c =
                              typeof a.getAttributeNode != "undefined" &&
                              a.getAttributeNode("id");
                            return a.nodeType === 1 && c && c.nodeValue === b;
                          })),
                        e.removeChild(a),
                        (e = a = null);
                    })(),
                    (function () {
                      var a = c.createElement("div");
                      a.appendChild(c.createComment("")),
                        a.getElementsByTagName("*").length > 0 &&
                          (o.find.TAG = function (a, b) {
                            var c = b.getElementsByTagName(a[1]);
                            if (a[1] === "*") {
                              var d = [];
                              for (var e = 0; c[e]; e++)
                                c[e].nodeType === 1 && d.push(c[e]);
                              c = d;
                            }
                            return c;
                          }),
                        (a.innerHTML = "<a href='#'></a>"),
                        a.firstChild &&
                          typeof a.firstChild.getAttribute != "undefined" &&
                          a.firstChild.getAttribute("href") !== "#" &&
                          (o.attrHandle.href = function (a) {
                            return a.getAttribute("href", 2);
                          }),
                        (a = null);
                    })(),
                    c.querySelectorAll &&
                      (function () {
                        var a = m,
                          b = c.createElement("div"),
                          d = "__sizzle__";
                        b.innerHTML = "<p class='TEST'></p>";
                        if (
                          !b.querySelectorAll ||
                          b.querySelectorAll(".TEST").length !== 0
                        ) {
                          m = function (b, e, f, g) {
                            e = e || c;
                            if (!g && !m.isXML(e)) {
                              var h = /^(\w+$)|^\.([\w\-]+$)|^#([\w\-]+$)/.exec(b);
                              if (h && (e.nodeType === 1 || e.nodeType === 9)) {
                                if (h[1]) return s(e.getElementsByTagName(b), f);
                                if (h[2] && o.find.CLASS && e.getElementsByClassName)
                                  return s(e.getElementsByClassName(h[2]), f);
                              }
                              if (e.nodeType === 9) {
                                if (b === "body" && e.body) return s([e.body], f);
                                if (h && h[3]) {
                                  var i = e.getElementById(h[3]);
                                  if (!i || !i.parentNode) return s([], f);
                                  if (i.id === h[3]) return s([i], f);
                                }
                                try {
                                  return s(e.querySelectorAll(b), f);
                                } catch (j) {}
                              } else if (
                                e.nodeType === 1 &&
                                e.nodeName.toLowerCase() !== "object"
                              ) {
                                var k = e,
                                  l = e.getAttribute("id"),
                                  n = l || d,
                                  p = e.parentNode,
                                  q = /^\s*[+~]/.test(b);
                                l ? (n = n.replace(/'/g, "\\$&")) : e.setAttribute("id", n),
                                  q && p && (e = e.parentNode);
                                try {
                                  if (!q || p)
                                    return s(
                                      e.querySelectorAll("[id='" + n + "'] " + b),
                                      f
                                    );
                                } catch (r) {
                                } finally {
                                  l || k.removeAttribute("id");
                                }
                              }
                            }
                            return a(b, e, f, g);
                          };
                          for (var e in a) m[e] = a[e];
                          b = null;
                        }
                      })(),
                    (function () {
                      var a = c.documentElement,
                        b =
                          a.matchesSelector ||
                          a.mozMatchesSelector ||
                          a.webkitMatchesSelector ||
                          a.msMatchesSelector;
                      if (b) {
                        var d = !b.call(c.createElement("div"), "div"),
                          e = !1;
                        try {
                          b.call(c.documentElement, "[test!='']:sizzle");
                        } catch (f) {
                          e = !0;
                        }
                        m.matchesSelector = function (a, c) {
                          c = c.replace(/\=\s*([^'"\]]*)\s*\]/g, "='$1']");
                          if (!m.isXML(a))
                            try {
                              if (e || (!o.match.PSEUDO.test(c) && !/!=/.test(c))) {
                                var f = b.call(a, c);
                                if (f || !d || (a.document && a.document.nodeType !== 11))
                                  return f;
                              }
                            } catch (g) {}
                          return m(c, null, null, [a]).length > 0;
                        };
                      }
                    })(),
                    (function () {
                      var a = c.createElement("div");
                      a.innerHTML = "<div class='test e'></div><div class='test'></div>";
                      if (
                        !!a.getElementsByClassName &&
                        a.getElementsByClassName("e").length !== 0
                      ) {
                        a.lastChild.className = "e";
                        if (a.getElementsByClassName("e").length === 1) return;
                        o.order.splice(1, 0, "CLASS"),
                          (o.find.CLASS = function (a, b, c) {
                            if (typeof b.getElementsByClassName != "undefined" && !c)
                              return b.getElementsByClassName(a[1]);
                          }),
                          (a = null);
                      }
                    })(),
                    c.documentElement.contains
                      ? (m.contains = function (a, b) {
                          return a !== b && (a.contains ? a.contains(b) : !0);
                        })
                      : c.documentElement.compareDocumentPosition
                      ? (m.contains = function (a, b) {
                          return !!(a.compareDocumentPosition(b) & 16);
                        })
                      : (m.contains = function () {
                          return !1;
                        }),
                    (m.isXML = function (a) {
                      var b = (a ? a.ownerDocument || a : 0).documentElement;
                      return b ? b.nodeName !== "HTML" : !1;
                    });
                  var y = function (a, b, c) {
                    var d,
                      e = [],
                      f = "",
                      g = b.nodeType ? [b] : b;
                    while ((d = o.match.PSEUDO.exec(a)))
                      (f += d[0]), (a = a.replace(o.match.PSEUDO, ""));
                    a = o.relative[a] ? a + "*" : a;
                    for (var h = 0, i = g.length; h < i; h++) m(a, g[h], e, c);
                    return m.filter(f, e);
                  };
                  (m.attr = f.attr),
                    (m.selectors.attrMap = {}),
                    (f.find = m),
                    (f.expr = m.selectors),
                    (f.expr[":"] = f.expr.filters),
                    (f.unique = m.uniqueSort),
                    (f.text = m.getText),
                    (f.isXMLDoc = m.isXML),
                    (f.contains = m.contains);
                })();
              var L = /Until$/,
                M = /^(?:parents|prevUntil|prevAll)/,
                N = /,/,
                O = /^.[^:#\[\.,]*$/,
                P = Array.prototype.slice,
                Q = f.expr.match.POS,
                R = { children: !0, contents: !0, next: !0, prev: !0 };
              f.fn.extend({
                find: function (a) {
                  var b = this,
                    c,
                    d;
                  if (typeof a != "string")
                    return f(a).filter(function () {
                      for (c = 0, d = b.length; c < d; c++)
                        if (f.contains(b[c], this)) return !0;
                    });
                  var e = this.pushStack("", "find", a),
                    g,
                    h,
                    i;
                  for (c = 0, d = this.length; c < d; c++) {
                    (g = e.length), f.find(a, this[c], e);
                    if (c > 0)
                      for (h = g; h < e.length; h++)
                        for (i = 0; i < g; i++)
                          if (e[i] === e[h]) {
                            e.splice(h--, 1);
                            break;
                          }
                  }
                  return e;
                },
                has: function (a) {
                  var b = f(a);
                  return this.filter(function () {
                    for (var a = 0, c = b.length; a < c; a++)
                      if (f.contains(this, b[a])) return !0;
                  });
                },
                not: function (a) {
                  return this.pushStack(T(this, a, !1), "not", a);
                },
                filter: function (a) {
                  return this.pushStack(T(this, a, !0), "filter", a);
                },
                is: function (a) {
                  return (
                    !!a &&
                    (typeof a == "string"
                      ? Q.test(a)
                        ? f(a, this.context).index(this[0]) >= 0
                        : f.filter(a, this).length > 0
                      : this.filter(a).length > 0)
                  );
                },
                closest: function (a, b) {
                  var c = [],
                    d,
                    e,
                    g = this[0];
                  if (f.isArray(a)) {
                    var h = 1;
                    while (g && g.ownerDocument && g !== b) {
                      for (d = 0; d < a.length; d++)
                        f(g).is(a[d]) && c.push({ selector: a[d], elem: g, level: h });
                      (g = g.parentNode), h++;
                    }
                    return c;
                  }
                  var i = Q.test(a) || typeof a != "string" ? f(a, b || this.context) : 0;
                  for (d = 0, e = this.length; d < e; d++) {
                    g = this[d];
                    while (g) {
                      if (i ? i.index(g) > -1 : f.find.matchesSelector(g, a)) {
                        c.push(g);
                        break;
                      }
                      g = g.parentNode;
                      if (!g || !g.ownerDocument || g === b || g.nodeType === 11) break;
                    }
                  }
                  c = c.length > 1 ? f.unique(c) : c;
                  return this.pushStack(c, "closest", a);
                },
                index: function (a) {
                  if (!a) return this[0] && this[0].parentNode ? this.prevAll().length : -1;
                  if (typeof a == "string") return f.inArray(this[0], f(a));
                  return f.inArray(a.jquery ? a[0] : a, this);
                },
                add: function (a, b) {
                  var c =
                      typeof a == "string"
                        ? f(a, b)
                        : f.makeArray(a && a.nodeType ? [a] : a),
                    d = f.merge(this.get(), c);
                  return this.pushStack(S(c[0]) || S(d[0]) ? d : f.unique(d));
                },
                andSelf: function () {
                  return this.add(this.prevObject);
                },
              }),
                f.each(
                  {
                    parent: function (a) {
                      var b = a.parentNode;
                      return b && b.nodeType !== 11 ? b : null;
                    },
                    parents: function (a) {
                      return f.dir(a, "parentNode");
                    },
                    parentsUntil: function (a, b, c) {
                      return f.dir(a, "parentNode", c);
                    },
                    next: function (a) {
                      return f.nth(a, 2, "nextSibling");
                    },
                    prev: function (a) {
                      return f.nth(a, 2, "previousSibling");
                    },
                    nextAll: function (a) {
                      return f.dir(a, "nextSibling");
                    },
                    prevAll: function (a) {
                      return f.dir(a, "previousSibling");
                    },
                    nextUntil: function (a, b, c) {
                      return f.dir(a, "nextSibling", c);
                    },
                    prevUntil: function (a, b, c) {
                      return f.dir(a, "previousSibling", c);
                    },
                    siblings: function (a) {
                      return f.sibling(a.parentNode.firstChild, a);
                    },
                    children: function (a) {
                      return f.sibling(a.firstChild);
                    },
                    contents: function (a) {
                      return f.nodeName(a, "iframe")
                        ? a.contentDocument || a.contentWindow.document
                        : f.makeArray(a.childNodes);
                    },
                  },
                  function (a, b) {
                    f.fn[a] = function (c, d) {
                      var e = f.map(this, b, c);
                      L.test(a) || (d = c),
                        d && typeof d == "string" && (e = f.filter(d, e)),
                        (e = this.length > 1 && !R[a] ? f.unique(e) : e),
                        (this.length > 1 || N.test(d)) && M.test(a) && (e = e.reverse());
                      return this.pushStack(e, a, P.call(arguments).join(","));
                    };
                  }
                ),
                f.extend({
                  filter: function (a, b, c) {
                    c && (a = ":not(" + a + ")");
                    return b.length === 1
                      ? f.find.matchesSelector(b[0], a)
                        ? [b[0]]
                        : []
                      : f.find.matches(a, b);
                  },
                  dir: function (a, c, d) {
                    var e = [],
                      g = a[c];
                    while (
                      g &&
                      g.nodeType !== 9 &&
                      (d === b || g.nodeType !== 1 || !f(g).is(d))
                    )
                      g.nodeType === 1 && e.push(g), (g = g[c]);
                    return e;
                  },
                  nth: function (a, b, c, d) {
                    b = b || 1;
                    var e = 0;
                    for (; a; a = a[c]) if (a.nodeType === 1 && ++e === b) break;
                    return a;
                  },
                  sibling: function (a, b) {
                    var c = [];
                    for (; a; a = a.nextSibling) a.nodeType === 1 && a !== b && c.push(a);
                    return c;
                  },
                });
              var V =
                  "abbr|article|aside|audio|canvas|datalist|details|figcaption|figure|footer|header|hgroup|mark|meter|nav|output|progress|section|summary|time|video",
                W = / jQuery\d+="(?:\d+|null)"/g,
                X = /^\s+/,
                Y =
                  /<(?!area|br|col|embed|hr|img|input|link|meta|param)(([\w:]+)[^>]*)\/>/gi,
                Z = /<([\w:]+)/,
                $ = /<tbody/i,
                _ = /<|&#?\w+;/,
                ba = /<(?:script|style)/i,
                bb = /<(?:script|object|embed|option|style)/i,
                bc = new RegExp("<(?:" + V + ")", "i"),
                bd = /checked\s*(?:[^=]|=\s*.checked.)/i,
                be = /\/(java|ecma)script/i,
                bf = /^\s*<!(?:\[CDATA\[|\-\-)/,
                bg = {
                  option: [1, "<select multiple='multiple'>", "</select>"],
                  legend: [1, "<fieldset>", "</fieldset>"],
                  thead: [1, "<table>", "</table>"],
                  tr: [2, "<table><tbody>", "</tbody></table>"],
                  td: [3, "<table><tbody><tr>", "</tr></tbody></table>"],
                  col: [2, "<table><tbody></tbody><colgroup>", "</colgroup></table>"],
                  area: [1, "<map>", "</map>"],
                  _default: [0, "", ""],
                },
                bh = U(c);
              (bg.optgroup = bg.option),
                (bg.tbody = bg.tfoot = bg.colgroup = bg.caption = bg.thead),
                (bg.th = bg.td),
                f.support.htmlSerialize || (bg._default = [1, "div<div>", "</div>"]),
                f.fn.extend({
                  text: function (a) {
                    if (f.isFunction(a))
                      return this.each(function (b) {
                        var c = f(this);
                        c.text(a.call(this, b, c.text()));
                      });
                    if (typeof a != "object" && a !== b)
                      return this.empty().append(
                        ((this[0] && this[0].ownerDocument) || c).createTextNode(a)
                      );
                    return f.text(this);
                  },
                  wrapAll: function (a) {
                    if (f.isFunction(a))
                      return this.each(function (b) {
                        f(this).wrapAll(a.call(this, b));
                      });
                    if (this[0]) {
                      var b = f(a, this[0].ownerDocument).eq(0).clone(!0);
                      this[0].parentNode && b.insertBefore(this[0]),
                        b
                          .map(function () {
                            var a = this;
                            while (a.firstChild && a.firstChild.nodeType === 1)
                              a = a.firstChild;
                            return a;
                          })
                          .append(this);
                    }
                    return this;
                  },
                  wrapInner: function (a) {
                    if (f.isFunction(a))
                      return this.each(function (b) {
                        f(this).wrapInner(a.call(this, b));
                      });
                    return this.each(function () {
                      var b = f(this),
                        c = b.contents();
                      c.length ? c.wrapAll(a) : b.append(a);
                    });
                  },
                  wrap: function (a) {
                    var b = f.isFunction(a);
                    return this.each(function (c) {
                      f(this).wrapAll(b ? a.call(this, c) : a);
                    });
                  },
                  unwrap: function () {
                    return this.parent()
                      .each(function () {
                        f.nodeName(this, "body") || f(this).replaceWith(this.childNodes);
                      })
                      .end();
                  },
                  append: function () {
                    return this.domManip(arguments, !0, function (a) {
                      this.nodeType === 1 && this.appendChild(a);
                    });
                  },
                  prepend: function () {
                    return this.domManip(arguments, !0, function (a) {
                      this.nodeType === 1 && this.insertBefore(a, this.firstChild);
                    });
                  },
                  before: function () {
                    if (this[0] && this[0].parentNode)
                      return this.domManip(arguments, !1, function (a) {
                        this.parentNode.insertBefore(a, this);
                      });
                    if (arguments.length) {
                      var a = f.clean(arguments);
                      a.push.apply(a, this.toArray());
                      return this.pushStack(a, "before", arguments);
                    }
                  },
                  after: function () {
                    if (this[0] && this[0].parentNode)
                      return this.domManip(arguments, !1, function (a) {
                        this.parentNode.insertBefore(a, this.nextSibling);
                      });
                    if (arguments.length) {
                      var a = this.pushStack(this, "after", arguments);
                      a.push.apply(a, f.clean(arguments));
                      return a;
                    }
                  },
                  remove: function (a, b) {
                    for (var c = 0, d; (d = this[c]) != null; c++)
                      if (!a || f.filter(a, [d]).length)
                        !b &&
                          d.nodeType === 1 &&
                          (f.cleanData(d.getElementsByTagName("*")), f.cleanData([d])),
                          d.parentNode && d.parentNode.removeChild(d);
                    return this;
                  },
                  empty: function () {
                    for (var a = 0, b; (b = this[a]) != null; a++) {
                      b.nodeType === 1 && f.cleanData(b.getElementsByTagName("*"));
                      while (b.firstChild) b.removeChild(b.firstChild);
                    }
                    return this;
                  },
                  clone: function (a, b) {
                    (a = a == null ? !1 : a), (b = b == null ? a : b);
                    return this.map(function () {
                      return f.clone(this, a, b);
                    });
                  },
                  html: function (a) {
                    if (a === b)
                      return this[0] && this[0].nodeType === 1
                        ? this[0].innerHTML.replace(W, "")
                        : null;
                    if (
                      typeof a == "string" &&
                      !ba.test(a) &&
                      (f.support.leadingWhitespace || !X.test(a)) &&
                      !bg[(Z.exec(a) || ["", ""])[1].toLowerCase()]
                    ) {
                      a = a.replace(Y, "<$1></$2>");
                      try {
                        for (var c = 0, d = this.length; c < d; c++)
                          this[c].nodeType === 1 &&
                            (f.cleanData(this[c].getElementsByTagName("*")),
                            (this[c].innerHTML = a));
                      } catch (e) {
                        this.empty().append(a);
                      }
                    } else
                      f.isFunction(a)
                        ? this.each(function (b) {
                            var c = f(this);
                            c.html(a.call(this, b, c.html()));
                          })
                        : this.empty().append(a);
                    return this;
                  },
                  replaceWith: function (a) {
                    if (this[0] && this[0].parentNode) {
                      if (f.isFunction(a))
                        return this.each(function (b) {
                          var c = f(this),
                            d = c.html();
                          c.replaceWith(a.call(this, b, d));
                        });
                      typeof a != "string" && (a = f(a).detach());
                      return this.each(function () {
                        var b = this.nextSibling,
                          c = this.parentNode;
                        f(this).remove(), b ? f(b).before(a) : f(c).append(a);
                      });
                    }
                    return this.length
                      ? this.pushStack(f(f.isFunction(a) ? a() : a), "replaceWith", a)
                      : this;
                  },
                  detach: function (a) {
                    return this.remove(a, !0);
                  },
                  domManip: function (a, c, d) {
                    var e,
                      g,
                      h,
                      i,
                      j = a[0],
                      k = [];
                    if (
                      !f.support.checkClone &&
                      arguments.length === 3 &&
                      typeof j == "string" &&
                      bd.test(j)
                    )
                      return this.each(function () {
                        f(this).domManip(a, c, d, !0);
                      });
                    if (f.isFunction(j))
                      return this.each(function (e) {
                        var g = f(this);
                        (a[0] = j.call(this, e, c ? g.html() : b)), g.domManip(a, c, d);
                      });
                    if (this[0]) {
                      (i = j && j.parentNode),
                        f.support.parentNode &&
                        i &&
                        i.nodeType === 11 &&
                        i.childNodes.length === this.length
                          ? (e = { fragment: i })
                          : (e = f.buildFragment(a, this, k)),
                        (h = e.fragment),
                        h.childNodes.length === 1
                          ? (g = h = h.firstChild)
                          : (g = h.firstChild);
                      if (g) {
                        c = c && f.nodeName(g, "tr");
                        for (var l = 0, m = this.length, n = m - 1; l < m; l++)
                          d.call(
                            c ? bi(this[l], g) : this[l],
                            e.cacheable || (m > 1 && l < n) ? f.clone(h, !0, !0) : h
                          );
                      }
                      k.length && f.each(k, bp);
                    }
                    return this;
                  },
                }),
                (f.buildFragment = function (a, b, d) {
                  var e,
                    g,
                    h,
                    i,
                    j = a[0];
                  b && b[0] && (i = b[0].ownerDocument || b[0]),
                    i.createDocumentFragment || (i = c),
                    a.length === 1 &&
                      typeof j == "string" &&
                      j.length < 512 &&
                      i === c &&
                      j.charAt(0) === "<" &&
                      !bb.test(j) &&
                      (f.support.checkClone || !bd.test(j)) &&
                      (f.support.html5Clone || !bc.test(j)) &&
                      ((g = !0), (h = f.fragments[j]), h && h !== 1 && (e = h)),
                    e || ((e = i.createDocumentFragment()), f.clean(a, i, e, d)),
                    g && (f.fragments[j] = h ? e : 1);
                  return { fragment: e, cacheable: g };
                }),
                (f.fragments = {}),
                f.each(
                  {
                    appendTo: "append",
                    prependTo: "prepend",
                    insertBefore: "before",
                    insertAfter: "after",
                    replaceAll: "replaceWith",
                  },
                  function (a, b) {
                    f.fn[a] = function (c) {
                      var d = [],
                        e = f(c),
                        g = this.length === 1 && this[0].parentNode;
                      if (
                        g &&
                        g.nodeType === 11 &&
                        g.childNodes.length === 1 &&
                        e.length === 1
                      ) {
                        e[b](this[0]);
                        return this;
                      }
                      for (var h = 0, i = e.length; h < i; h++) {
                        var j = (h > 0 ? this.clone(!0) : this).get();
                        f(e[h])[b](j), (d = d.concat(j));
                      }
                      return this.pushStack(d, a, e.selector);
                    };
                  }
                ),
                f.extend({
                  clone: function (a, b, c) {
                    var d,
                      e,
                      g,
                      h =
                        f.support.html5Clone || !bc.test("<" + a.nodeName)
                          ? a.cloneNode(!0)
                          : bo(a);
                    if (
                      (!f.support.noCloneEvent || !f.support.noCloneChecked) &&
                      (a.nodeType === 1 || a.nodeType === 11) &&
                      !f.isXMLDoc(a)
                    ) {
                      bk(a, h), (d = bl(a)), (e = bl(h));
                      for (g = 0; d[g]; ++g) e[g] && bk(d[g], e[g]);
                    }
                    if (b) {
                      bj(a, h);
                      if (c) {
                        (d = bl(a)), (e = bl(h));
                        for (g = 0; d[g]; ++g) bj(d[g], e[g]);
                      }
                    }
                    d = e = null;
                    return h;
                  },
                  clean: function (a, b, d, e) {
                    var g;
                    (b = b || c),
                      typeof b.createElement == "undefined" &&
                        (b = b.ownerDocument || (b[0] && b[0].ownerDocument) || c);
                    var h = [],
                      i;
                    for (var j = 0, k; (k = a[j]) != null; j++) {
                      typeof k == "number" && (k += "");
                      if (!k) continue;
                      if (typeof k == "string")
                        if (!_.test(k)) k = b.createTextNode(k);
                        else {
                          k = k.replace(Y, "<$1></$2>");
                          var l = (Z.exec(k) || ["", ""])[1].toLowerCase(),
                            m = bg[l] || bg._default,
                            n = m[0],
                            o = b.createElement("div");
                          b === c ? bh.appendChild(o) : U(b).appendChild(o),
                            (o.innerHTML = m[1] + k + m[2]);
                          while (n--) o = o.lastChild;
                          if (!f.support.tbody) {
                            var p = $.test(k),
                              q =
                                l === "table" && !p
                                  ? o.firstChild && o.firstChild.childNodes
                                  : m[1] === "<table>" && !p
                                  ? o.childNodes
                                  : [];
                            for (i = q.length - 1; i >= 0; --i)
                              f.nodeName(q[i], "tbody") &&
                                !q[i].childNodes.length &&
                                q[i].parentNode.removeChild(q[i]);
                          }
                          !f.support.leadingWhitespace &&
                            X.test(k) &&
                            o.insertBefore(b.createTextNode(X.exec(k)[0]), o.firstChild),
                            (k = o.childNodes);
                        }
                      var r;
                      if (!f.support.appendChecked)
                        if (k[0] && typeof (r = k.length) == "number")
                          for (i = 0; i < r; i++) bn(k[i]);
                        else bn(k);
                      k.nodeType ? h.push(k) : (h = f.merge(h, k));
                    }
                    if (d) {
                      g = function (a) {
                        return !a.type || be.test(a.type);
                      };
                      for (j = 0; h[j]; j++)
                        if (
                          e &&
                          f.nodeName(h[j], "script") &&
                          (!h[j].type || h[j].type.toLowerCase() === "text/javascript")
                        )
                          e.push(
                            h[j].parentNode ? h[j].parentNode.removeChild(h[j]) : h[j]
                          );
                        else {
                          if (h[j].nodeType === 1) {
                            var s = f.grep(h[j].getElementsByTagName("script"), g);
                            h.splice.apply(h, [j + 1, 0].concat(s));
                          }
                          d.appendChild(h[j]);
                        }
                    }
                    return h;
                  },
                  cleanData: function (a) {
                    var b,
                      c,
                      d = f.cache,
                      e = f.event.special,
                      g = f.support.deleteExpando;
                    for (var h = 0, i; (i = a[h]) != null; h++) {
                      if (i.nodeName && f.noData[i.nodeName.toLowerCase()]) continue;
                      c = i[f.expando];
                      if (c) {
                        b = d[c];
                        if (b && b.events) {
                          for (var j in b.events)
                            e[j] ? f.event.remove(i, j) : f.removeEvent(i, j, b.handle);
                          b.handle && (b.handle.elem = null);
                        }
                        g
                          ? delete i[f.expando]
                          : i.removeAttribute && i.removeAttribute(f.expando),
                          delete d[c];
                      }
                    }
                  },
                });
              var bq = /alpha\([^)]*\)/i,
                br = /opacity=([^)]*)/,
                bs = /([A-Z]|^ms)/g,
                bt = /^-?\d+(?:px)?$/i,
                bu = /^-?\d/,
                bv = /^([\-+])=([\-+.\de]+)/,
                bw = { position: "absolute", visibility: "hidden", display: "block" },
                bx = ["Left", "Right"],
                by = ["Top", "Bottom"],
                bz,
                bA,
                bB;
              (f.fn.css = function (a, c) {
                if (arguments.length === 2 && c === b) return this;
                return f.access(this, a, c, !0, function (a, c, d) {
                  return d !== b ? f.style(a, c, d) : f.css(a, c);
                });
              }),
                f.extend({
                  cssHooks: {
                    opacity: {
                      get: function (a, b) {
                        if (b) {
                          var c = bz(a, "opacity", "opacity");
                          return c === "" ? "1" : c;
                        }
                        return a.style.opacity;
                      },
                    },
                  },
                  cssNumber: {
                    fillOpacity: !0,
                    fontWeight: !0,
                    lineHeight: !0,
                    opacity: !0,
                    orphans: !0,
                    widows: !0,
                    zIndex: !0,
                    zoom: !0,
                  },
                  cssProps: { float: f.support.cssFloat ? "cssFloat" : "styleFloat" },
                  style: function (a, c, d, e) {
                    if (!!a && a.nodeType !== 3 && a.nodeType !== 8 && !!a.style) {
                      var g,
                        h,
                        i = f.camelCase(c),
                        j = a.style,
                        k = f.cssHooks[i];
                      c = f.cssProps[i] || i;
                      if (d === b) {
                        if (k && "get" in k && (g = k.get(a, !1, e)) !== b) return g;
                        return j[c];
                      }
                      (h = typeof d),
                        h === "string" &&
                          (g = bv.exec(d)) &&
                          ((d = +(g[1] + 1) * +g[2] + parseFloat(f.css(a, c))),
                          (h = "number"));
                      if (d == null || (h === "number" && isNaN(d))) return;
                      h === "number" && !f.cssNumber[i] && (d += "px");
                      if (!k || !("set" in k) || (d = k.set(a, d)) !== b)
                        try {
                          j[c] = d;
                        } catch (l) {}
                    }
                  },
                  css: function (a, c, d) {
                    var e, g;
                    (c = f.camelCase(c)),
                      (g = f.cssHooks[c]),
                      (c = f.cssProps[c] || c),
                      c === "cssFloat" && (c = "float");
                    if (g && "get" in g && (e = g.get(a, !0, d)) !== b) return e;
                    if (bz) return bz(a, c);
                  },
                  swap: function (a, b, c) {
                    var d = {};
                    for (var e in b) (d[e] = a.style[e]), (a.style[e] = b[e]);
                    c.call(a);
                    for (e in b) a.style[e] = d[e];
                  },
                }),
                (f.curCSS = f.css),
                f.each(["height", "width"], function (a, b) {
                  f.cssHooks[b] = {
                    get: function (a, c, d) {
                      var e;
                      if (c) {
                        if (a.offsetWidth !== 0) return bC(a, b, d);
                        f.swap(a, bw, function () {
                          e = bC(a, b, d);
                        });
                        return e;
                      }
                    },
                    set: function (a, b) {
                      if (!bt.test(b)) return b;
                      b = parseFloat(b);
                      if (b >= 0) return b + "px";
                    },
                  };
                }),
                f.support.opacity ||
                  (f.cssHooks.opacity = {
                    get: function (a, b) {
                      return br.test(
                        (b && a.currentStyle ? a.currentStyle.filter : a.style.filter) || ""
                      )
                        ? parseFloat(RegExp.$1) / 100 + ""
                        : b
                        ? "1"
                        : "";
                    },
                    set: function (a, b) {
                      var c = a.style,
                        d = a.currentStyle,
                        e = f.isNumeric(b) ? "alpha(opacity=" + b * 100 + ")" : "",
                        g = (d && d.filter) || c.filter || "";
                      c.zoom = 1;
                      if (b >= 1 && f.trim(g.replace(bq, "")) === "") {
                        c.removeAttribute("filter");
                        if (d && !d.filter) return;
                      }
                      c.filter = bq.test(g) ? g.replace(bq, e) : g + " " + e;
                    },
                  }),
                f(function () {
                  f.support.reliableMarginRight ||
                    (f.cssHooks.marginRight = {
                      get: function (a, b) {
                        var c;
                        f.swap(a, { display: "inline-block" }, function () {
                          b
                            ? (c = bz(a, "margin-right", "marginRight"))
                            : (c = a.style.marginRight);
                        });
                        return c;
                      },
                    });
                }),
                c.defaultView &&
                  c.defaultView.getComputedStyle &&
                  (bA = function (a, b) {
                    var c, d, e;
                    (b = b.replace(bs, "-$1").toLowerCase()),
                      (d = a.ownerDocument.defaultView) &&
                        (e = d.getComputedStyle(a, null)) &&
                        ((c = e.getPropertyValue(b)),
                        c === "" &&
                          !f.contains(a.ownerDocument.documentElement, a) &&
                          (c = f.style(a, b)));
                    return c;
                  }),
                c.documentElement.currentStyle &&
                  (bB = function (a, b) {
                    var c,
                      d,
                      e,
                      f = a.currentStyle && a.currentStyle[b],
                      g = a.style;
                    f === null && g && (e = g[b]) && (f = e),
                      !bt.test(f) &&
                        bu.test(f) &&
                        ((c = g.left),
                        (d = a.runtimeStyle && a.runtimeStyle.left),
                        d && (a.runtimeStyle.left = a.currentStyle.left),
                        (g.left = b === "fontSize" ? "1em" : f || 0),
                        (f = g.pixelLeft + "px"),
                        (g.left = c),
                        d && (a.runtimeStyle.left = d));
                    return f === "" ? "auto" : f;
                  }),
                (bz = bA || bB),
                f.expr &&
                  f.expr.filters &&
                  ((f.expr.filters.hidden = function (a) {
                    var b = a.offsetWidth,
                      c = a.offsetHeight;
                    return (
                      (b === 0 && c === 0) ||
                      (!f.support.reliableHiddenOffsets &&
                        ((a.style && a.style.display) || f.css(a, "display")) === "none")
                    );
                  }),
                  (f.expr.filters.visible = function (a) {
                    return !f.expr.filters.hidden(a);
                  }));
              var bD = /%20/g,
                bE = /\[\]$/,
                bF = /\r?\n/g,
                bG = /#.*$/,
                bH = /^(.*?):[ \t]*([^\r\n]*)\r?$/gm,
                bI =
                  /^(?:color|date|datetime|datetime-local|email|hidden|month|number|password|range|search|tel|text|time|url|week)$/i,
                bJ = /^(?:about|app|app\-storage|.+\-extension|file|res|widget):$/,
                bK = /^(?:GET|HEAD)$/,
                bL = /^\/\//,
                bM = /\?/,
                bN = /<script\b[^<]*(?:(?!<\/script>)<[^<]*)*<\/script>/gi,
                bO = /^(?:select|textarea)/i,
                bP = /\s+/,
                bQ = /([?&])_=[^&]*/,
                bR = /^([\w\+\.\-]+:)(?:\/\/([^\/?#:]*)(?::(\d+))?)?/,
                bS = f.fn.load,
                bT = {},
                bU = {},
                bV,
                bW,
                bX = ["*/"] + ["*"];
              try {
                bV = e.href;
              } catch (bY) {
                (bV = c.createElement("a")), (bV.href = ""), (bV = bV.href);
              }
              (bW = bR.exec(bV.toLowerCase()) || []),
                f.fn.extend({
                  load: function (a, c, d) {
                    if (typeof a != "string" && bS) return bS.apply(this, arguments);
                    if (!this.length) return this;
                    var e = a.indexOf(" ");
                    if (e >= 0) {
                      var g = a.slice(e, a.length);
                      a = a.slice(0, e);
                    }
                    var h = "GET";
                    c &&
                      (f.isFunction(c)
                        ? ((d = c), (c = b))
                        : typeof c == "object" &&
                          ((c = f.param(c, f.ajaxSettings.traditional)), (h = "POST")));
                    var i = this;
                    f.ajax({
                      url: a,
                      type: h,
                      dataType: "html",
                      data: c,
                      complete: function (a, b, c) {
                        (c = a.responseText),
                          a.isResolved() &&
                            (a.done(function (a) {
                              c = a;
                            }),
                            i.html(g ? f("<div>").append(c.replace(bN, "")).find(g) : c)),
                          d && i.each(d, [c, b, a]);
                      },
                    });
                    return this;
                  },
                  serialize: function () {
                    return f.param(this.serializeArray());
                  },
                  serializeArray: function () {
                    return this.map(function () {
                      return this.elements ? f.makeArray(this.elements) : this;
                    })
                      .filter(function () {
                        return (
                          this.name &&
                          !this.disabled &&
                          (this.checked || bO.test(this.nodeName) || bI.test(this.type))
                        );
                      })
                      .map(function (a, b) {
                        var c = f(this).val();
                        return c == null
                          ? null
                          : f.isArray(c)
                          ? f.map(c, function (a, c) {
                              return { name: b.name, value: a.replace(bF, "\r\n") };
                            })
                          : { name: b.name, value: c.replace(bF, "\r\n") };
                      })
                      .get();
                  },
                }),
                f.each(
                  "ajaxStart ajaxStop ajaxComplete ajaxError ajaxSuccess ajaxSend".split(
                    " "
                  ),
                  function (a, b) {
                    f.fn[b] = function (a) {
                      return this.on(b, a);
                    };
                  }
                ),
                f.each(["get", "post"], function (a, c) {
                  f[c] = function (a, d, e, g) {
                    f.isFunction(d) && ((g = g || e), (e = d), (d = b));
                    return f.ajax({ type: c, url: a, data: d, success: e, dataType: g });
                  };
                }),
                f.extend({
                  getScript: function (a, c) {
                    return f.get(a, b, c, "script");
                  },
                  getJSON: function (a, b, c) {
                    return f.get(a, b, c, "json");
                  },
                  ajaxSetup: function (a, b) {
                    b ? b_(a, f.ajaxSettings) : ((b = a), (a = f.ajaxSettings)), b_(a, b);
                    return a;
                  },
                  ajaxSettings: {
                    url: bV,
                    isLocal: bJ.test(bW[1]),
                    global: !0,
                    type: "GET",
                    contentType: "application/x-www-form-urlencoded",
                    processData: !0,
                    async: !0,
                    accepts: {
                      xml: "application/xml, text/xml",
                      html: "text/html",
                      text: "text/plain",
                      json: "application/json, text/javascript",
                      "*": bX,
                    },
                    contents: { xml: /xml/, html: /html/, json: /json/ },
                    responseFields: { xml: "responseXML", text: "responseText" },
                    converters: {
                      "* text": a.String,
                      "text html": !0,
                      "text json": f.parseJSON,
                      "text xml": f.parseXML,
                    },
                    flatOptions: { context: !0, url: !0 },
                  },
                  ajaxPrefilter: bZ(bT),
                  ajaxTransport: bZ(bU),
                  ajax: function (a, c) {
                    function w(a, c, l, m) {
                      if (s !== 2) {
                        (s = 2),
                          q && clearTimeout(q),
                          (p = b),
                          (n = m || ""),
                          (v.readyState = a > 0 ? 4 : 0);
                        var o,
                          r,
                          u,
                          w = c,
                          x = l ? cb(d, v, l) : b,
                          y,
                          z;
                        if ((a >= 200 && a < 300) || a === 304) {
                          if (d.ifModified) {
                            if ((y = v.getResponseHeader("Last-Modified")))
                              f.lastModified[k] = y;
                            if ((z = v.getResponseHeader("Etag"))) f.etag[k] = z;
                          }
                          if (a === 304) (w = "notmodified"), (o = !0);
                          else
                            try {
                              (r = cc(d, x)), (w = "success"), (o = !0);
                            } catch (A) {
                              (w = "parsererror"), (u = A);
                            }
                        } else {
                          u = w;
                          if (!w || a) (w = "error"), a < 0 && (a = 0);
                        }
                        (v.status = a),
                          (v.statusText = "" + (c || w)),
                          o ? h.resolveWith(e, [r, w, v]) : h.rejectWith(e, [v, w, u]),
                          v.statusCode(j),
                          (j = b),
                          t &&
                            g.trigger("ajax" + (o ? "Success" : "Error"), [
                              v,
                              d,
                              o ? r : u,
                            ]),
                          i.fireWith(e, [v, w]),
                          t &&
                            (g.trigger("ajaxComplete", [v, d]),
                            --f.active || f.event.trigger("ajaxStop"));
                      }
                    }
                    typeof a == "object" && ((c = a), (a = b)), (c = c || {});
                    var d = f.ajaxSetup({}, c),
                      e = d.context || d,
                      g = e !== d && (e.nodeType || e instanceof f) ? f(e) : f.event,
                      h = f.Deferred(),
                      i = f.Callbacks("once memory"),
                      j = d.statusCode || {},
                      k,
                      l = {},
                      m = {},
                      n,
                      o,
                      p,
                      q,
                      r,
                      s = 0,
                      t,
                      u,
                      v = {
                        readyState: 0,
                        setRequestHeader: function (a, b) {
                          if (!s) {
                            var c = a.toLowerCase();
                            (a = m[c] = m[c] || a), (l[a] = b);
                          }
                          return this;
                        },
                        getAllResponseHeaders: function () {
                          return s === 2 ? n : null;
                        },
                        getResponseHeader: function (a) {
                          var c;
                          if (s === 2) {
                            if (!o) {
                              o = {};
                              while ((c = bH.exec(n))) o[c[1].toLowerCase()] = c[2];
                            }
                            c = o[a.toLowerCase()];
                          }
                          return c === b ? null : c;
                        },
                        overrideMimeType: function (a) {
                          s || (d.mimeType = a);
                          return this;
                        },
                        abort: function (a) {
                          (a = a || "abort"), p && p.abort(a), w(0, a);
                          return this;
                        },
                      };
                    h.promise(v),
                      (v.success = v.done),
                      (v.error = v.fail),
                      (v.complete = i.add),
                      (v.statusCode = function (a) {
                        if (a) {
                          var b;
                          if (s < 2) for (b in a) j[b] = [j[b], a[b]];
                          else (b = a[v.status]), v.then(b, b);
                        }
                        return this;
                      }),
                      (d.url = ((a || d.url) + "")
                        .replace(bG, "")
                        .replace(bL, bW[1] + "//")),
                      (d.dataTypes = f
                        .trim(d.dataType || "*")
                        .toLowerCase()
                        .split(bP)),
                      d.crossDomain == null &&
                        ((r = bR.exec(d.url.toLowerCase())),
                        (d.crossDomain = !(
                          !r ||
                          (r[1] == bW[1] &&
                            r[2] == bW[2] &&
                            (r[3] || (r[1] === "http:" ? 80 : 443)) ==
                              (bW[3] || (bW[1] === "http:" ? 80 : 443)))
                        ))),
                      d.data &&
                        d.processData &&
                        typeof d.data != "string" &&
                        (d.data = f.param(d.data, d.traditional)),
                      b$(bT, d, c, v);
                    if (s === 2) return !1;
                    (t = d.global),
                      (d.type = d.type.toUpperCase()),
                      (d.hasContent = !bK.test(d.type)),
                      t && f.active++ === 0 && f.event.trigger("ajaxStart");
                    if (!d.hasContent) {
                      d.data &&
                        ((d.url += (bM.test(d.url) ? "&" : "?") + d.data), delete d.data),
                        (k = d.url);
                      if (d.cache === !1) {
                        var x = f.now(),
                          y = d.url.replace(bQ, "$1_=" + x);
                        d.url =
                          y + (y === d.url ? (bM.test(d.url) ? "&" : "?") + "_=" + x : "");
                      }
                    }
                    ((d.data && d.hasContent && d.contentType !== !1) || c.contentType) &&
                      v.setRequestHeader("Content-Type", d.contentType),
                      d.ifModified &&
                        ((k = k || d.url),
                        f.lastModified[k] &&
                          v.setRequestHeader("If-Modified-Since", f.lastModified[k]),
                        f.etag[k] && v.setRequestHeader("If-None-Match", f.etag[k])),
                      v.setRequestHeader(
                        "Accept",
                        d.dataTypes[0] && d.accepts[d.dataTypes[0]]
                          ? d.accepts[d.dataTypes[0]] +
                              (d.dataTypes[0] !== "*" ? ", " + bX + "; q=0.01" : "")
                          : d.accepts["*"]
                      );
                    for (u in d.headers) v.setRequestHeader(u, d.headers[u]);
                    if (d.beforeSend && (d.beforeSend.call(e, v, d) === !1 || s === 2)) {
                      v.abort();
                      return !1;
                    }
                    for (u in { success: 1, error: 1, complete: 1 }) v[u](d[u]);
                    p = b$(bU, d, c, v);
                    if (!p) w(-1, "No Transport");
                    else {
                      (v.readyState = 1),
                        t && g.trigger("ajaxSend", [v, d]),
                        d.async &&
                          d.timeout > 0 &&
                          (q = setTimeout(function () {
                            v.abort("timeout");
                          }, d.timeout));
                      try {
                        (s = 1), p.send(l, w);
                      } catch (z) {
                        if (s < 2) w(-1, z);
                        else throw z;
                      }
                    }
                    return v;
                  },
                  param: function (a, c) {
                    var d = [],
                      e = function (a, b) {
                        (b = f.isFunction(b) ? b() : b),
                          (d[d.length] =
                            encodeURIComponent(a) + "=" + encodeURIComponent(b));
                      };
                    c === b && (c = f.ajaxSettings.traditional);
                    if (f.isArray(a) || (a.jquery && !f.isPlainObject(a)))
                      f.each(a, function () {
                        e(this.name, this.value);
                      });
                    else for (var g in a) ca(g, a[g], c, e);
                    return d.join("&").replace(bD, "+");
                  },
                }),
                f.extend({ active: 0, lastModified: {}, etag: {} });
              var cd = f.now(),
                ce = /(\=)\?(&|$)|\?\?/i;
              f.ajaxSetup({
                jsonp: "callback",
                jsonpCallback: function () {
                  return f.expando + "_" + cd++;
                },
              }),
                f.ajaxPrefilter("json jsonp", function (b, c, d) {
                  var e =
                    b.contentType === "application/x-www-form-urlencoded" &&
                    typeof b.data == "string";
                  if (
                    b.dataTypes[0] === "jsonp" ||
                    (b.jsonp !== !1 && (ce.test(b.url) || (e && ce.test(b.data))))
                  ) {
                    var g,
                      h = (b.jsonpCallback = f.isFunction(b.jsonpCallback)
                        ? b.jsonpCallback()
                        : b.jsonpCallback),
                      i = a[h],
                      j = b.url,
                      k = b.data,
                      l = "$1" + h + "$2";
                    b.jsonp !== !1 &&
                      ((j = j.replace(ce, l)),
                      b.url === j &&
                        (e && (k = k.replace(ce, l)),
                        b.data === k &&
                          (j += (/\?/.test(j) ? "&" : "?") + b.jsonp + "=" + h))),
                      (b.url = j),
                      (b.data = k),
                      (a[h] = function (a) {
                        g = [a];
                      }),
                      d.always(function () {
                        (a[h] = i), g && f.isFunction(i) && a[h](g[0]);
                      }),
                      (b.converters["script json"] = function () {
                        g || f.error(h + " was not called");
                        return g[0];
                      }),
                      (b.dataTypes[0] = "json");
                    return "script";
                  }
                }),
                f.ajaxSetup({
                  accepts: {
                    script:
                      "text/javascript, application/javascript, application/ecmascript, application/x-ecmascript",
                  },
                  contents: { script: /javascript|ecmascript/ },
                  converters: {
                    "text script": function (a) {
                      f.globalEval(a);
                      return a;
                    },
                  },
                }),
                f.ajaxPrefilter("script", function (a) {
                  a.cache === b && (a.cache = !1),
                    a.crossDomain && ((a.type = "GET"), (a.global = !1));
                }),
                f.ajaxTransport("script", function (a) {
                  if (a.crossDomain) {
                    var d,
                      e = c.head || c.getElementsByTagName("head")[0] || c.documentElement;
                    return {
                      send: function (f, g) {
                        (d = c.createElement("script")),
                          (d.async = "async"),
                          a.scriptCharset && (d.charset = a.scriptCharset),
                          (d.src = a.url),
                          (d.onload = d.onreadystatechange =
                            function (a, c) {
                              if (
                                c ||
                                !d.readyState ||
                                /loaded|complete/.test(d.readyState)
                              )
                                (d.onload = d.onreadystatechange = null),
                                  e && d.parentNode && e.removeChild(d),
                                  (d = b),
                                  c || g(200, "success");
                            }),
                          e.insertBefore(d, e.firstChild);
                      },
                      abort: function () {
                        d && d.onload(0, 1);
                      },
                    };
                  }
                });
              var cf = a.ActiveXObject
                  ? function () {
                      for (var a in ch) ch[a](0, 1);
                    }
                  : !1,
                cg = 0,
                ch;
              (f.ajaxSettings.xhr = a.ActiveXObject
                ? function () {
                    return (!this.isLocal && ci()) || cj();
                  }
                : ci),
                (function (a) {
                  f.extend(f.support, { ajax: !!a, cors: !!a && "withCredentials" in a });
                })(f.ajaxSettings.xhr()),
                f.support.ajax &&
                  f.ajaxTransport(function (c) {
                    if (!c.crossDomain || f.support.cors) {
                      var d;
                      return {
                        send: function (e, g) {
                          var h = c.xhr(),
                            i,
                            j;
                          c.username
                            ? h.open(c.type, c.url, c.async, c.username, c.password)
                            : h.open(c.type, c.url, c.async);
                          if (c.xhrFields) for (j in c.xhrFields) h[j] = c.xhrFields[j];
                          c.mimeType &&
                            h.overrideMimeType &&
                            h.overrideMimeType(c.mimeType),
                            !c.crossDomain &&
                              !e["X-Requested-With"] &&
                              (e["X-Requested-With"] = "XMLHttpRequest");
                          try {
                            for (j in e) h.setRequestHeader(j, e[j]);
                          } catch (k) {}
                          h.send((c.hasContent && c.data) || null),
                            (d = function (a, e) {
                              var j, k, l, m, n;
                              try {
                                if (d && (e || h.readyState === 4)) {
                                  (d = b),
                                    i &&
                                      ((h.onreadystatechange = f.noop), cf && delete ch[i]);
                                  if (e) h.readyState !== 4 && h.abort();
                                  else {
                                    (j = h.status),
                                      (l = h.getAllResponseHeaders()),
                                      (m = {}),
                                      (n = h.responseXML),
                                      n && n.documentElement && (m.xml = n),
                                      (m.text = h.responseText);
                                    try {
                                      k = h.statusText;
                                    } catch (o) {
                                      k = "";
                                    }
                                    !j && c.isLocal && !c.crossDomain
                                      ? (j = m.text ? 200 : 404)
                                      : j === 1223 && (j = 204);
                                  }
                                }
                              } catch (p) {
                                e || g(-1, p);
                              }
                              m && g(j, k, m, l);
                            }),
                            !c.async || h.readyState === 4
                              ? d()
                              : ((i = ++cg),
                                cf && (ch || ((ch = {}), f(a).unload(cf)), (ch[i] = d)),
                                (h.onreadystatechange = d));
                        },
                        abort: function () {
                          d && d(0, 1);
                        },
                      };
                    }
                  });
              var ck = {},
                cl,
                cm,
                cn = /^(?:toggle|show|hide)$/,
                co = /^([+\-]=)?([\d+.\-]+)([a-z%]*)$/i,
                cp,
                cq = [
                  ["height", "marginTop", "marginBottom", "paddingTop", "paddingBottom"],
                  ["width", "marginLeft", "marginRight", "paddingLeft", "paddingRight"],
                  ["opacity"],
                ],
                cr;
              f.fn.extend({
                show: function (a, b, c) {
                  var d, e;
                  if (a || a === 0) return this.animate(cu("show", 3), a, b, c);
                  for (var g = 0, h = this.length; g < h; g++)
                    (d = this[g]),
                      d.style &&
                        ((e = d.style.display),
                        !f._data(d, "olddisplay") &&
                          e === "none" &&
                          (e = d.style.display = ""),
                        e === "" &&
                          f.css(d, "display") === "none" &&
                          f._data(d, "olddisplay", cv(d.nodeName)));
                  for (g = 0; g < h; g++) {
                    d = this[g];
                    if (d.style) {
                      e = d.style.display;
                      if (e === "" || e === "none")
                        d.style.display = f._data(d, "olddisplay") || "";
                    }
                  }
                  return this;
                },
                hide: function (a, b, c) {
                  if (a || a === 0) return this.animate(cu("hide", 3), a, b, c);
                  var d,
                    e,
                    g = 0,
                    h = this.length;
                  for (; g < h; g++)
                    (d = this[g]),
                      d.style &&
                        ((e = f.css(d, "display")),
                        e !== "none" &&
                          !f._data(d, "olddisplay") &&
                          f._data(d, "olddisplay", e));
                  for (g = 0; g < h; g++) this[g].style && (this[g].style.display = "none");
                  return this;
                },
                _toggle: f.fn.toggle,
                toggle: function (a, b, c) {
                  var d = typeof a == "boolean";
                  f.isFunction(a) && f.isFunction(b)
                    ? this._toggle.apply(this, arguments)
                    : a == null || d
                    ? this.each(function () {
                        var b = d ? a : f(this).is(":hidden");
                        f(this)[b ? "show" : "hide"]();
                      })
                    : this.animate(cu("toggle", 3), a, b, c);
                  return this;
                },
                fadeTo: function (a, b, c, d) {
                  return this.filter(":hidden")
                    .css("opacity", 0)
                    .show()
                    .end()
                    .animate({ opacity: b }, a, c, d);
                },
                animate: function (a, b, c, d) {
                  function g() {
                    e.queue === !1 && f._mark(this);
                    var b = f.extend({}, e),
                      c = this.nodeType === 1,
                      d = c && f(this).is(":hidden"),
                      g,
                      h,
                      i,
                      j,
                      k,
                      l,
                      m,
                      n,
                      o;
                    b.animatedProperties = {};
                    for (i in a) {
                      (g = f.camelCase(i)),
                        i !== g && ((a[g] = a[i]), delete a[i]),
                        (h = a[g]),
                        f.isArray(h)
                          ? ((b.animatedProperties[g] = h[1]), (h = a[g] = h[0]))
                          : (b.animatedProperties[g] =
                              (b.specialEasing && b.specialEasing[g]) ||
                              b.easing ||
                              "swing");
                      if ((h === "hide" && d) || (h === "show" && !d))
                        return b.complete.call(this);
                      c &&
                        (g === "height" || g === "width") &&
                        ((b.overflow = [
                          this.style.overflow,
                          this.style.overflowX,
                          this.style.overflowY,
                        ]),
                        f.css(this, "display") === "inline" &&
                          f.css(this, "float") === "none" &&
                          (!f.support.inlineBlockNeedsLayout ||
                          cv(this.nodeName) === "inline"
                            ? (this.style.display = "inline-block")
                            : (this.style.zoom = 1)));
                    }
                    b.overflow != null && (this.style.overflow = "hidden");
                    for (i in a)
                      (j = new f.fx(this, b, i)),
                        (h = a[i]),
                        cn.test(h)
                          ? ((o =
                              f._data(this, "toggle" + i) ||
                              (h === "toggle" ? (d ? "show" : "hide") : 0)),
                            o
                              ? (f._data(
                                  this,
                                  "toggle" + i,
                                  o === "show" ? "hide" : "show"
                                ),
                                j[o]())
                              : j[h]())
                          : ((k = co.exec(h)),
                            (l = j.cur()),
                            k
                              ? ((m = parseFloat(k[2])),
                                (n = k[3] || (f.cssNumber[i] ? "" : "px")),
                                n !== "px" &&
                                  (f.style(this, i, (m || 1) + n),
                                  (l = ((m || 1) / j.cur()) * l),
                                  f.style(this, i, l + n)),
                                k[1] && (m = (k[1] === "-=" ? -1 : 1) * m + l),
                                j.custom(l, m, n))
                              : j.custom(l, h, ""));
                    return !0;
                  }
                  var e = f.speed(b, c, d);
                  if (f.isEmptyObject(a)) return this.each(e.complete, [!1]);
                  a = f.extend({}, a);
                  return e.queue === !1 ? this.each(g) : this.queue(e.queue, g);
                },
                stop: function (a, c, d) {
                  typeof a != "string" && ((d = c), (c = a), (a = b)),
                    c && a !== !1 && this.queue(a || "fx", []);
                  return this.each(function () {
                    function h(a, b, c) {
                      var e = b[c];
                      f.removeData(a, c, !0), e.stop(d);
                    }
                    var b,
                      c = !1,
                      e = f.timers,
                      g = f._data(this);
                    d || f._unmark(!0, this);
                    if (a == null)
                      for (b in g)
                        g[b] &&
                          g[b].stop &&
                          b.indexOf(".run") === b.length - 4 &&
                          h(this, g, b);
                    else g[(b = a + ".run")] && g[b].stop && h(this, g, b);
                    for (b = e.length; b--; )
                      e[b].elem === this &&
                        (a == null || e[b].queue === a) &&
                        (d ? e[b](!0) : e[b].saveState(), (c = !0), e.splice(b, 1));
                    (!d || !c) && f.dequeue(this, a);
                  });
                },
              }),
                f.each(
                  {
                    slideDown: cu("show", 1),
                    slideUp: cu("hide", 1),
                    slideToggle: cu("toggle", 1),
                    fadeIn: { opacity: "show" },
                    fadeOut: { opacity: "hide" },
                    fadeToggle: { opacity: "toggle" },
                  },
                  function (a, b) {
                    f.fn[a] = function (a, c, d) {
                      return this.animate(b, a, c, d);
                    };
                  }
                ),
                f.extend({
                  speed: function (a, b, c) {
                    var d =
                      a && typeof a == "object"
                        ? f.extend({}, a)
                        : {
                            complete: c || (!c && b) || (f.isFunction(a) && a),
                            duration: a,
                            easing: (c && b) || (b && !f.isFunction(b) && b),
                          };
                    d.duration = f.fx.off
                      ? 0
                      : typeof d.duration == "number"
                      ? d.duration
                      : d.duration in f.fx.speeds
                      ? f.fx.speeds[d.duration]
                      : f.fx.speeds._default;
                    if (d.queue == null || d.queue === !0) d.queue = "fx";
                    (d.old = d.complete),
                      (d.complete = function (a) {
                        f.isFunction(d.old) && d.old.call(this),
                          d.queue ? f.dequeue(this, d.queue) : a !== !1 && f._unmark(this);
                      });
                    return d;
                  },
                  easing: {
                    linear: function (a, b, c, d) {
                      return c + d * a;
                    },
                    swing: function (a, b, c, d) {
                      return (-Math.cos(a * Math.PI) / 2 + 0.5) * d + c;
                    },
                  },
                  timers: [],
                  fx: function (a, b, c) {
                    (this.options = b),
                      (this.elem = a),
                      (this.prop = c),
                      (b.orig = b.orig || {});
                  },
                }),
                (f.fx.prototype = {
                  update: function () {
                    this.options.step && this.options.step.call(this.elem, this.now, this),
                      (f.fx.step[this.prop] || f.fx.step._default)(this);
                  },
                  cur: function () {
                    if (
                      this.elem[this.prop] != null &&
                      (!this.elem.style || this.elem.style[this.prop] == null)
                    )
                      return this.elem[this.prop];
                    var a,
                      b = f.css(this.elem, this.prop);
                    return isNaN((a = parseFloat(b))) ? (!b || b === "auto" ? 0 : b) : a;
                  },
                  custom: function (a, c, d) {
                    function h(a) {
                      return e.step(a);
                    }
                    var e = this,
                      g = f.fx;
                    (this.startTime = cr || cs()),
                      (this.end = c),
                      (this.now = this.start = a),
                      (this.pos = this.state = 0),
                      (this.unit = d || this.unit || (f.cssNumber[this.prop] ? "" : "px")),
                      (h.queue = this.options.queue),
                      (h.elem = this.elem),
                      (h.saveState = function () {
                        e.options.hide &&
                          f._data(e.elem, "fxshow" + e.prop) === b &&
                          f._data(e.elem, "fxshow" + e.prop, e.start);
                      }),
                      h() &&
                        f.timers.push(h) &&
                        !cp &&
                        (cp = setInterval(g.tick, g.interval));
                  },
                  show: function () {
                    var a = f._data(this.elem, "fxshow" + this.prop);
                    (this.options.orig[this.prop] = a || f.style(this.elem, this.prop)),
                      (this.options.show = !0),
                      a !== b
                        ? this.custom(this.cur(), a)
                        : this.custom(
                            this.prop === "width" || this.prop === "height" ? 1 : 0,
                            this.cur()
                          ),
                      f(this.elem).show();
                  },
                  hide: function () {
                    (this.options.orig[this.prop] =
                      f._data(this.elem, "fxshow" + this.prop) ||
                      f.style(this.elem, this.prop)),
                      (this.options.hide = !0),
                      this.custom(this.cur(), 0);
                  },
                  step: function (a) {
                    var b,
                      c,
                      d,
                      e = cr || cs(),
                      g = !0,
                      h = this.elem,
                      i = this.options;
                    if (a || e >= i.duration + this.startTime) {
                      (this.now = this.end),
                        (this.pos = this.state = 1),
                        this.update(),
                        (i.animatedProperties[this.prop] = !0);
                      for (b in i.animatedProperties)
                        i.animatedProperties[b] !== !0 && (g = !1);
                      if (g) {
                        i.overflow != null &&
                          !f.support.shrinkWrapBlocks &&
                          f.each(["", "X", "Y"], function (a, b) {
                            h.style["overflow" + b] = i.overflow[a];
                          }),
                          i.hide && f(h).hide();
                        if (i.hide || i.show)
                          for (b in i.animatedProperties)
                            f.style(h, b, i.orig[b]),
                              f.removeData(h, "fxshow" + b, !0),
                              f.removeData(h, "toggle" + b, !0);
                        (d = i.complete), d && ((i.complete = !1), d.call(h));
                      }
                      return !1;
                    }
                    i.duration == Infinity
                      ? (this.now = e)
                      : ((c = e - this.startTime),
                        (this.state = c / i.duration),
                        (this.pos = f.easing[i.animatedProperties[this.prop]](
                          this.state,
                          c,
                          0,
                          1,
                          i.duration
                        )),
                        (this.now = this.start + (this.end - this.start) * this.pos)),
                      this.update();
                    return !0;
                  },
                }),
                f.extend(f.fx, {
                  tick: function () {
                    var a,
                      b = f.timers,
                      c = 0;
                    for (; c < b.length; c++)
                      (a = b[c]), !a() && b[c] === a && b.splice(c--, 1);
                    b.length || f.fx.stop();
                  },
                  interval: 13,
                  stop: function () {
                    clearInterval(cp), (cp = null);
                  },
                  speeds: { slow: 600, fast: 200, _default: 400 },
                  step: {
                    opacity: function (a) {
                      f.style(a.elem, "opacity", a.now);
                    },
                    _default: function (a) {
                      a.elem.style && a.elem.style[a.prop] != null
                        ? (a.elem.style[a.prop] = a.now + a.unit)
                        : (a.elem[a.prop] = a.now);
                    },
                  },
                }),
                f.each(["width", "height"], function (a, b) {
                  f.fx.step[b] = function (a) {
                    f.style(a.elem, b, Math.max(0, a.now) + a.unit);
                  };
                }),
                f.expr &&
                  f.expr.filters &&
                  (f.expr.filters.animated = function (a) {
                    return f.grep(f.timers, function (b) {
                      return a === b.elem;
                    }).length;
                  });
              var cw = /^t(?:able|d|h)$/i,
                cx = /^(?:body|html)$/i;
              "getBoundingClientRect" in c.documentElement
                ? (f.fn.offset = function (a) {
                    var b = this[0],
                      c;
                    if (a)
                      return this.each(function (b) {
                        f.offset.setOffset(this, a, b);
                      });
                    if (!b || !b.ownerDocument) return null;
                    if (b === b.ownerDocument.body) return f.offset.bodyOffset(b);
                    try {
                      c = b.getBoundingClientRect();
                    } catch (d) {}
                    var e = b.ownerDocument,
                      g = e.documentElement;
                    if (!c || !f.contains(g, b))
                      return c ? { top: c.top, left: c.left } : { top: 0, left: 0 };
                    var h = e.body,
                      i = cy(e),
                      j = g.clientTop || h.clientTop || 0,
                      k = g.clientLeft || h.clientLeft || 0,
                      l =
                        i.pageYOffset || (f.support.boxModel && g.scrollTop) || h.scrollTop,
                      m =
                        i.pageXOffset ||
                        (f.support.boxModel && g.scrollLeft) ||
                        h.scrollLeft,
                      n = c.top + l - j,
                      o = c.left + m - k;
                    return { top: n, left: o };
                  })
                : (f.fn.offset = function (a) {
                    var b = this[0];
                    if (a)
                      return this.each(function (b) {
                        f.offset.setOffset(this, a, b);
                      });
                    if (!b || !b.ownerDocument) return null;
                    if (b === b.ownerDocument.body) return f.offset.bodyOffset(b);
                    var c,
                      d = b.offsetParent,
                      e = b,
                      g = b.ownerDocument,
                      h = g.documentElement,
                      i = g.body,
                      j = g.defaultView,
                      k = j ? j.getComputedStyle(b, null) : b.currentStyle,
                      l = b.offsetTop,
                      m = b.offsetLeft;
                    while ((b = b.parentNode) && b !== i && b !== h) {
                      if (f.support.fixedPosition && k.position === "fixed") break;
                      (c = j ? j.getComputedStyle(b, null) : b.currentStyle),
                        (l -= b.scrollTop),
                        (m -= b.scrollLeft),
                        b === d &&
                          ((l += b.offsetTop),
                          (m += b.offsetLeft),
                          f.support.doesNotAddBorder &&
                            (!f.support.doesAddBorderForTableAndCells ||
                              !cw.test(b.nodeName)) &&
                            ((l += parseFloat(c.borderTopWidth) || 0),
                            (m += parseFloat(c.borderLeftWidth) || 0)),
                          (e = d),
                          (d = b.offsetParent)),
                        f.support.subtractsBorderForOverflowNotVisible &&
                          c.overflow !== "visible" &&
                          ((l += parseFloat(c.borderTopWidth) || 0),
                          (m += parseFloat(c.borderLeftWidth) || 0)),
                        (k = c);
                    }
                    if (k.position === "relative" || k.position === "static")
                      (l += i.offsetTop), (m += i.offsetLeft);
                    f.support.fixedPosition &&
                      k.position === "fixed" &&
                      ((l += Math.max(h.scrollTop, i.scrollTop)),
                      (m += Math.max(h.scrollLeft, i.scrollLeft)));
                    return { top: l, left: m };
                  }),
                (f.offset = {
                  bodyOffset: function (a) {
                    var b = a.offsetTop,
                      c = a.offsetLeft;
                    f.support.doesNotIncludeMarginInBodyOffset &&
                      ((b += parseFloat(f.css(a, "marginTop")) || 0),
                      (c += parseFloat(f.css(a, "marginLeft")) || 0));
                    return { top: b, left: c };
                  },
                  setOffset: function (a, b, c) {
                    var d = f.css(a, "position");
                    d === "static" && (a.style.position = "relative");
                    var e = f(a),
                      g = e.offset(),
                      h = f.css(a, "top"),
                      i = f.css(a, "left"),
                      j =
                        (d === "absolute" || d === "fixed") &&
                        f.inArray("auto", [h, i]) > -1,
                      k = {},
                      l = {},
                      m,
                      n;
                    j
                      ? ((l = e.position()), (m = l.top), (n = l.left))
                      : ((m = parseFloat(h) || 0), (n = parseFloat(i) || 0)),
                      f.isFunction(b) && (b = b.call(a, c, g)),
                      b.top != null && (k.top = b.top - g.top + m),
                      b.left != null && (k.left = b.left - g.left + n),
                      "using" in b ? b.using.call(a, k) : e.css(k);
                  },
                }),
                f.fn.extend({
                  position: function () {
                    if (!this[0]) return null;
                    var a = this[0],
                      b = this.offsetParent(),
                      c = this.offset(),
                      d = cx.test(b[0].nodeName) ? { top: 0, left: 0 } : b.offset();
                    (c.top -= parseFloat(f.css(a, "marginTop")) || 0),
                      (c.left -= parseFloat(f.css(a, "marginLeft")) || 0),
                      (d.top += parseFloat(f.css(b[0], "borderTopWidth")) || 0),
                      (d.left += parseFloat(f.css(b[0], "borderLeftWidth")) || 0);
                    return { top: c.top - d.top, left: c.left - d.left };
                  },
                  offsetParent: function () {
                    return this.map(function () {
                      var a = this.offsetParent || c.body;
                      while (a && !cx.test(a.nodeName) && f.css(a, "position") === "static")
                        a = a.offsetParent;
                      return a;
                    });
                  },
                }),
                f.each(["Left", "Top"], function (a, c) {
                  var d = "scroll" + c;
                  f.fn[d] = function (c) {
                    var e, g;
                    if (c === b) {
                      e = this[0];
                      if (!e) return null;
                      g = cy(e);
                      return g
                        ? "pageXOffset" in g
                          ? g[a ? "pageYOffset" : "pageXOffset"]
                          : (f.support.boxModel && g.document.documentElement[d]) ||
                            g.document.body[d]
                        : e[d];
                    }
                    return this.each(function () {
                      (g = cy(this)),
                        g
                          ? g.scrollTo(a ? f(g).scrollLeft() : c, a ? c : f(g).scrollTop())
                          : (this[d] = c);
                    });
                  };
                }),
                f.each(["Height", "Width"], function (a, c) {
                  var d = c.toLowerCase();
                  (f.fn["inner" + c] = function () {
                    var a = this[0];
                    return a
                      ? a.style
                        ? parseFloat(f.css(a, d, "padding"))
                        : this[d]()
                      : null;
                  }),
                    (f.fn["outer" + c] = function (a) {
                      var b = this[0];
                      return b
                        ? b.style
                          ? parseFloat(f.css(b, d, a ? "margin" : "border"))
                          : this[d]()
                        : null;
                    }),
                    (f.fn[d] = function (a) {
                      var e = this[0];
                      if (!e) return a == null ? null : this;
                      if (f.isFunction(a))
                        return this.each(function (b) {
                          var c = f(this);
                          c[d](a.call(this, b, c[d]()));
                        });
                      if (f.isWindow(e)) {
                        var g = e.document.documentElement["client" + c],
                          h = e.document.body;
                        return (
                          (e.document.compatMode === "CSS1Compat" && g) ||
                          (h && h["client" + c]) ||
                          g
                        );
                      }
                      if (e.nodeType === 9)
                        return Math.max(
                          e.documentElement["client" + c],
                          e.body["scroll" + c],
                          e.documentElement["scroll" + c],
                          e.body["offset" + c],
                          e.documentElement["offset" + c]
                        );
                      if (a === b) {
                        var i = f.css(e, d),
                          j = parseFloat(i);
                        return f.isNumeric(j) ? j : i;
                      }
                      return this.css(d, typeof a == "string" ? a : a + "px");
                    });
                }),
                (a.jQuery = a.$ = f),
                typeof define == "function" &&
                  define.amd &&
                  define.amd.jQuery &&
                  define("jquery", [], function () {
                    return f;
                  });
            })(window);
            </script>
		<script> (function(){var b={DEBUG:1,INFO:2,WARN:3,ERROR:4},d=function(){this.level=b.WARN};d.prototype={log:function(a){try{console.log(a)}catch(b){}},debug:function(a){this.level<=b.DEBUG&&this.log(a)},info:function(a){this.level<=b.INFO&&this.log(a)},warn:function(a){this.level<=b.WARN&&this.log(a)},error:function(a){this.level<=b.ERROR&&this.log(a)}};var e=function(a){var b=[],c;for(c in a)b.push(c);return b},c=function(a){a._forInKeys=e;a.Logging={Logger:d,Level:b};a.logger=new d;a.modules={};a.binders=
            {};a.builders={}},f=typeof define==="function"&&!define.amd,g=typeof require==="function"&&typeof define==="function"&&define.amd;typeof require==="function"&&typeof module!=="undefined"&&module.exports?c(module.exports):f?define("jscex",function(a,b,d){c(d.exports)}):g?define("jscex",function(){var a={};c(a);return a}):(typeof Jscex=="undefined"&&(Jscex={}),c(Jscex))})();
            </script>
		<script> /***********************************************************************

            A JavaScript tokenizer / parser / beautifier / compressor.
          
            This version is suitable for Node.js.  With minimal changes (the
            exports stuff) it should work on any JS platform.
          
            This file contains the tokenizer/parser.  It is a port to JavaScript
            of parse-js [1], a JavaScript parser library written in Common Lisp
            by Marijn Haverbeke.  Thank you Marijn!
          
            [1] http://marijn.haverbeke.nl/parse-js/
          
            Exported functions:
          
              - tokenizer(code) -- returns a function.  Call the returned
                function to fetch the next token.
          
              - parse(code) -- returns an AST of the given JavaScript code.
          
            -------------------------------- (C) ---------------------------------
          
                                     Author: Mihai Bazon
                                   <mihai.bazon@gmail.com>
                                 http://mihai.bazon.net/blog
          
            Distributed under the BSD license:
          
              Copyright 2010 (c) Mihai Bazon <mihai.bazon@gmail.com>
              Based on parse-js (http://marijn.haverbeke.nl/parse-js/).
          
              Redistribution and use in source and binary forms, with or without
              modification, are permitted provided that the following conditions
              are met:
          
                  * Redistributions of source code must retain the above
                    copyright notice, this list of conditions and the following
                    disclaimer.
          
                  * Redistributions in binary form must reproduce the above
                    copyright notice, this list of conditions and the following
                    disclaimer in the documentation and/or other materials
                    provided with the distribution.
          
              THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDER “AS IS” AND ANY
              EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
              IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR
              PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER BE
              LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY,
              OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
              PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR
              PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
              THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR
              TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF
              THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
              SUCH DAMAGE.
          
           ***********************************************************************/
          
          (function () {
          
          /* -----[ Tokenizer (constants) ]----- */
          
          var KEYWORDS = array_to_hash([
                  "break",
                  "case",
                  "catch",
                  "const",
                  "continue",
                  "default",
                  "delete",
                  "do",
                  "else",
                  "finally",
                  "for",
                  "function",
                  "if",
                  "in",
                  "instanceof",
                  "new",
                  "return",
                  "switch",
                  "throw",
                  "try",
                  "typeof",
                  "var",
                  "void",
                  "while",
                  "with"
          ]);
          
          var RESERVED_WORDS = array_to_hash([
                  "abstract",
                  "boolean",
                  "byte",
                  "char",
                  "class",
                  "debugger",
                  "double",
                  "enum",
                  "export",
                  "extends",
                  "final",
                  "float",
                  "goto",
                  "implements",
                  "import",
                  "int",
                  "interface",
                  "long",
                  "native",
                  "package",
                  "private",
                  "protected",
                  "public",
                  "short",
                  "static",
                  "super",
                  "synchronized",
                  "throws",
                  "transient",
                  "volatile"
          ]);
          
          var KEYWORDS_BEFORE_EXPRESSION = array_to_hash([
                  "return",
                  "new",
                  "delete",
                  "throw",
                  "else",
                  "case"
          ]);
          
          var KEYWORDS_ATOM = array_to_hash([
                  "false",
                  "null",
                  "true",
                  "undefined"
          ]);
          
          var OPERATOR_CHARS = array_to_hash(characters("+-*&%=<>!?|~^"));
          
          var RE_HEX_NUMBER = /^0x[0-9a-f]+$/i;
          var RE_OCT_NUMBER = /^0[0-7]+$/;
          var RE_DEC_NUMBER = /^\d*\.?\d*(?:e[+-]?\d*(?:\d\.?|\.?\d)\d*)?$/i;
          
          var OPERATORS = array_to_hash([
                  "in",
                  "instanceof",
                  "typeof",
                  "new",
                  "void",
                  "delete",
                  "++",
                  "--",
                  "+",
                  "-",
                  "!",
                  "~",
                  "&",
                  "|",
                  "^",
                  "*",
                  "/",
                  "%",
                  ">>",
                  "<<",
                  ">>>",
                  "<",
                  ">",
                  "<=",
                  ">=",
                  "==",
                  "===",
                  "!=",
                  "!==",
                  "?",
                  "=",
                  "+=",
                  "-=",
                  "/=",
                  "*=",
                  "%=",
                  ">>=",
                  "<<=",
                  ">>>=",
                  "|=",
                  "^=",
                  "&=",
                  "&&",
                  "||"
          ]);
          
          var WHITESPACE_CHARS = array_to_hash(characters(" \n\r\t\u200b"));
          
          var PUNC_BEFORE_EXPRESSION = array_to_hash(characters("[{}(,.;:"));
          
          var PUNC_CHARS = array_to_hash(characters("[]{}(),;:"));
          
          var REGEXP_MODIFIERS = array_to_hash(characters("gmsiy"));
          
          /* -----[ Tokenizer ]----- */
          
          // regexps adapted from http://xregexp.com/plugins/#unicode
          var UNICODE = {
                  letter: new RegExp("[\\u0041-\\u005A\\u0061-\\u007A\\u00AA\\u00B5\\u00BA\\u00C0-\\u00D6\\u00D8-\\u00F6\\u00F8-\\u02C1\\u02C6-\\u02D1\\u02E0-\\u02E4\\u02EC\\u02EE\\u0370-\\u0374\\u0376\\u0377\\u037A-\\u037D\\u0386\\u0388-\\u038A\\u038C\\u038E-\\u03A1\\u03A3-\\u03F5\\u03F7-\\u0481\\u048A-\\u0523\\u0531-\\u0556\\u0559\\u0561-\\u0587\\u05D0-\\u05EA\\u05F0-\\u05F2\\u0621-\\u064A\\u066E\\u066F\\u0671-\\u06D3\\u06D5\\u06E5\\u06E6\\u06EE\\u06EF\\u06FA-\\u06FC\\u06FF\\u0710\\u0712-\\u072F\\u074D-\\u07A5\\u07B1\\u07CA-\\u07EA\\u07F4\\u07F5\\u07FA\\u0904-\\u0939\\u093D\\u0950\\u0958-\\u0961\\u0971\\u0972\\u097B-\\u097F\\u0985-\\u098C\\u098F\\u0990\\u0993-\\u09A8\\u09AA-\\u09B0\\u09B2\\u09B6-\\u09B9\\u09BD\\u09CE\\u09DC\\u09DD\\u09DF-\\u09E1\\u09F0\\u09F1\\u0A05-\\u0A0A\\u0A0F\\u0A10\\u0A13-\\u0A28\\u0A2A-\\u0A30\\u0A32\\u0A33\\u0A35\\u0A36\\u0A38\\u0A39\\u0A59-\\u0A5C\\u0A5E\\u0A72-\\u0A74\\u0A85-\\u0A8D\\u0A8F-\\u0A91\\u0A93-\\u0AA8\\u0AAA-\\u0AB0\\u0AB2\\u0AB3\\u0AB5-\\u0AB9\\u0ABD\\u0AD0\\u0AE0\\u0AE1\\u0B05-\\u0B0C\\u0B0F\\u0B10\\u0B13-\\u0B28\\u0B2A-\\u0B30\\u0B32\\u0B33\\u0B35-\\u0B39\\u0B3D\\u0B5C\\u0B5D\\u0B5F-\\u0B61\\u0B71\\u0B83\\u0B85-\\u0B8A\\u0B8E-\\u0B90\\u0B92-\\u0B95\\u0B99\\u0B9A\\u0B9C\\u0B9E\\u0B9F\\u0BA3\\u0BA4\\u0BA8-\\u0BAA\\u0BAE-\\u0BB9\\u0BD0\\u0C05-\\u0C0C\\u0C0E-\\u0C10\\u0C12-\\u0C28\\u0C2A-\\u0C33\\u0C35-\\u0C39\\u0C3D\\u0C58\\u0C59\\u0C60\\u0C61\\u0C85-\\u0C8C\\u0C8E-\\u0C90\\u0C92-\\u0CA8\\u0CAA-\\u0CB3\\u0CB5-\\u0CB9\\u0CBD\\u0CDE\\u0CE0\\u0CE1\\u0D05-\\u0D0C\\u0D0E-\\u0D10\\u0D12-\\u0D28\\u0D2A-\\u0D39\\u0D3D\\u0D60\\u0D61\\u0D7A-\\u0D7F\\u0D85-\\u0D96\\u0D9A-\\u0DB1\\u0DB3-\\u0DBB\\u0DBD\\u0DC0-\\u0DC6\\u0E01-\\u0E30\\u0E32\\u0E33\\u0E40-\\u0E46\\u0E81\\u0E82\\u0E84\\u0E87\\u0E88\\u0E8A\\u0E8D\\u0E94-\\u0E97\\u0E99-\\u0E9F\\u0EA1-\\u0EA3\\u0EA5\\u0EA7\\u0EAA\\u0EAB\\u0EAD-\\u0EB0\\u0EB2\\u0EB3\\u0EBD\\u0EC0-\\u0EC4\\u0EC6\\u0EDC\\u0EDD\\u0F00\\u0F40-\\u0F47\\u0F49-\\u0F6C\\u0F88-\\u0F8B\\u1000-\\u102A\\u103F\\u1050-\\u1055\\u105A-\\u105D\\u1061\\u1065\\u1066\\u106E-\\u1070\\u1075-\\u1081\\u108E\\u10A0-\\u10C5\\u10D0-\\u10FA\\u10FC\\u1100-\\u1159\\u115F-\\u11A2\\u11A8-\\u11F9\\u1200-\\u1248\\u124A-\\u124D\\u1250-\\u1256\\u1258\\u125A-\\u125D\\u1260-\\u1288\\u128A-\\u128D\\u1290-\\u12B0\\u12B2-\\u12B5\\u12B8-\\u12BE\\u12C0\\u12C2-\\u12C5\\u12C8-\\u12D6\\u12D8-\\u1310\\u1312-\\u1315\\u1318-\\u135A\\u1380-\\u138F\\u13A0-\\u13F4\\u1401-\\u166C\\u166F-\\u1676\\u1681-\\u169A\\u16A0-\\u16EA\\u1700-\\u170C\\u170E-\\u1711\\u1720-\\u1731\\u1740-\\u1751\\u1760-\\u176C\\u176E-\\u1770\\u1780-\\u17B3\\u17D7\\u17DC\\u1820-\\u1877\\u1880-\\u18A8\\u18AA\\u1900-\\u191C\\u1950-\\u196D\\u1970-\\u1974\\u1980-\\u19A9\\u19C1-\\u19C7\\u1A00-\\u1A16\\u1B05-\\u1B33\\u1B45-\\u1B4B\\u1B83-\\u1BA0\\u1BAE\\u1BAF\\u1C00-\\u1C23\\u1C4D-\\u1C4F\\u1C5A-\\u1C7D\\u1D00-\\u1DBF\\u1E00-\\u1F15\\u1F18-\\u1F1D\\u1F20-\\u1F45\\u1F48-\\u1F4D\\u1F50-\\u1F57\\u1F59\\u1F5B\\u1F5D\\u1F5F-\\u1F7D\\u1F80-\\u1FB4\\u1FB6-\\u1FBC\\u1FBE\\u1FC2-\\u1FC4\\u1FC6-\\u1FCC\\u1FD0-\\u1FD3\\u1FD6-\\u1FDB\\u1FE0-\\u1FEC\\u1FF2-\\u1FF4\\u1FF6-\\u1FFC\\u2071\\u207F\\u2090-\\u2094\\u2102\\u2107\\u210A-\\u2113\\u2115\\u2119-\\u211D\\u2124\\u2126\\u2128\\u212A-\\u212D\\u212F-\\u2139\\u213C-\\u213F\\u2145-\\u2149\\u214E\\u2183\\u2184\\u2C00-\\u2C2E\\u2C30-\\u2C5E\\u2C60-\\u2C6F\\u2C71-\\u2C7D\\u2C80-\\u2CE4\\u2D00-\\u2D25\\u2D30-\\u2D65\\u2D6F\\u2D80-\\u2D96\\u2DA0-\\u2DA6\\u2DA8-\\u2DAE\\u2DB0-\\u2DB6\\u2DB8-\\u2DBE\\u2DC0-\\u2DC6\\u2DC8-\\u2DCE\\u2DD0-\\u2DD6\\u2DD8-\\u2DDE\\u2E2F\\u3005\\u3006\\u3031-\\u3035\\u303B\\u303C\\u3041-\\u3096\\u309D-\\u309F\\u30A1-\\u30FA\\u30FC-\\u30FF\\u3105-\\u312D\\u3131-\\u318E\\u31A0-\\u31B7\\u31F0-\\u31FF\\u3400\\u4DB5\\u4E00\\u9FC3\\uA000-\\uA48C\\uA500-\\uA60C\\uA610-\\uA61F\\uA62A\\uA62B\\uA640-\\uA65F\\uA662-\\uA66E\\uA67F-\\uA697\\uA717-\\uA71F\\uA722-\\uA788\\uA78B\\uA78C\\uA7FB-\\uA801\\uA803-\\uA805\\uA807-\\uA80A\\uA80C-\\uA822\\uA840-\\uA873\\uA882-\\uA8B3\\uA90A-\\uA925\\uA930-\\uA946\\uAA00-\\uAA28\\uAA40-\\uAA42\\uAA44-\\uAA4B\\uAC00\\uD7A3\\uF900-\\uFA2D\\uFA30-\\uFA6A\\uFA70-\\uFAD9\\uFB00-\\uFB06\\uFB13-\\uFB17\\uFB1D\\uFB1F-\\uFB28\\uFB2A-\\uFB36\\uFB38-\\uFB3C\\uFB3E\\uFB40\\uFB41\\uFB43\\uFB44\\uFB46-\\uFBB1\\uFBD3-\\uFD3D\\uFD50-\\uFD8F\\uFD92-\\uFDC7\\uFDF0-\\uFDFB\\uFE70-\\uFE74\\uFE76-\\uFEFC\\uFF21-\\uFF3A\\uFF41-\\uFF5A\\uFF66-\\uFFBE\\uFFC2-\\uFFC7\\uFFCA-\\uFFCF\\uFFD2-\\uFFD7\\uFFDA-\\uFFDC]"),
                  non_spacing_mark: new RegExp("[\\u0300-\\u036F\\u0483-\\u0487\\u0591-\\u05BD\\u05BF\\u05C1\\u05C2\\u05C4\\u05C5\\u05C7\\u0610-\\u061A\\u064B-\\u065E\\u0670\\u06D6-\\u06DC\\u06DF-\\u06E4\\u06E7\\u06E8\\u06EA-\\u06ED\\u0711\\u0730-\\u074A\\u07A6-\\u07B0\\u07EB-\\u07F3\\u0816-\\u0819\\u081B-\\u0823\\u0825-\\u0827\\u0829-\\u082D\\u0900-\\u0902\\u093C\\u0941-\\u0948\\u094D\\u0951-\\u0955\\u0962\\u0963\\u0981\\u09BC\\u09C1-\\u09C4\\u09CD\\u09E2\\u09E3\\u0A01\\u0A02\\u0A3C\\u0A41\\u0A42\\u0A47\\u0A48\\u0A4B-\\u0A4D\\u0A51\\u0A70\\u0A71\\u0A75\\u0A81\\u0A82\\u0ABC\\u0AC1-\\u0AC5\\u0AC7\\u0AC8\\u0ACD\\u0AE2\\u0AE3\\u0B01\\u0B3C\\u0B3F\\u0B41-\\u0B44\\u0B4D\\u0B56\\u0B62\\u0B63\\u0B82\\u0BC0\\u0BCD\\u0C3E-\\u0C40\\u0C46-\\u0C48\\u0C4A-\\u0C4D\\u0C55\\u0C56\\u0C62\\u0C63\\u0CBC\\u0CBF\\u0CC6\\u0CCC\\u0CCD\\u0CE2\\u0CE3\\u0D41-\\u0D44\\u0D4D\\u0D62\\u0D63\\u0DCA\\u0DD2-\\u0DD4\\u0DD6\\u0E31\\u0E34-\\u0E3A\\u0E47-\\u0E4E\\u0EB1\\u0EB4-\\u0EB9\\u0EBB\\u0EBC\\u0EC8-\\u0ECD\\u0F18\\u0F19\\u0F35\\u0F37\\u0F39\\u0F71-\\u0F7E\\u0F80-\\u0F84\\u0F86\\u0F87\\u0F90-\\u0F97\\u0F99-\\u0FBC\\u0FC6\\u102D-\\u1030\\u1032-\\u1037\\u1039\\u103A\\u103D\\u103E\\u1058\\u1059\\u105E-\\u1060\\u1071-\\u1074\\u1082\\u1085\\u1086\\u108D\\u109D\\u135F\\u1712-\\u1714\\u1732-\\u1734\\u1752\\u1753\\u1772\\u1773\\u17B7-\\u17BD\\u17C6\\u17C9-\\u17D3\\u17DD\\u180B-\\u180D\\u18A9\\u1920-\\u1922\\u1927\\u1928\\u1932\\u1939-\\u193B\\u1A17\\u1A18\\u1A56\\u1A58-\\u1A5E\\u1A60\\u1A62\\u1A65-\\u1A6C\\u1A73-\\u1A7C\\u1A7F\\u1B00-\\u1B03\\u1B34\\u1B36-\\u1B3A\\u1B3C\\u1B42\\u1B6B-\\u1B73\\u1B80\\u1B81\\u1BA2-\\u1BA5\\u1BA8\\u1BA9\\u1C2C-\\u1C33\\u1C36\\u1C37\\u1CD0-\\u1CD2\\u1CD4-\\u1CE0\\u1CE2-\\u1CE8\\u1CED\\u1DC0-\\u1DE6\\u1DFD-\\u1DFF\\u20D0-\\u20DC\\u20E1\\u20E5-\\u20F0\\u2CEF-\\u2CF1\\u2DE0-\\u2DFF\\u302A-\\u302F\\u3099\\u309A\\uA66F\\uA67C\\uA67D\\uA6F0\\uA6F1\\uA802\\uA806\\uA80B\\uA825\\uA826\\uA8C4\\uA8E0-\\uA8F1\\uA926-\\uA92D\\uA947-\\uA951\\uA980-\\uA982\\uA9B3\\uA9B6-\\uA9B9\\uA9BC\\uAA29-\\uAA2E\\uAA31\\uAA32\\uAA35\\uAA36\\uAA43\\uAA4C\\uAAB0\\uAAB2-\\uAAB4\\uAAB7\\uAAB8\\uAABE\\uAABF\\uAAC1\\uABE5\\uABE8\\uABED\\uFB1E\\uFE00-\\uFE0F\\uFE20-\\uFE26]"),
                  space_combining_mark: new RegExp("[\\u0903\\u093E-\\u0940\\u0949-\\u094C\\u094E\\u0982\\u0983\\u09BE-\\u09C0\\u09C7\\u09C8\\u09CB\\u09CC\\u09D7\\u0A03\\u0A3E-\\u0A40\\u0A83\\u0ABE-\\u0AC0\\u0AC9\\u0ACB\\u0ACC\\u0B02\\u0B03\\u0B3E\\u0B40\\u0B47\\u0B48\\u0B4B\\u0B4C\\u0B57\\u0BBE\\u0BBF\\u0BC1\\u0BC2\\u0BC6-\\u0BC8\\u0BCA-\\u0BCC\\u0BD7\\u0C01-\\u0C03\\u0C41-\\u0C44\\u0C82\\u0C83\\u0CBE\\u0CC0-\\u0CC4\\u0CC7\\u0CC8\\u0CCA\\u0CCB\\u0CD5\\u0CD6\\u0D02\\u0D03\\u0D3E-\\u0D40\\u0D46-\\u0D48\\u0D4A-\\u0D4C\\u0D57\\u0D82\\u0D83\\u0DCF-\\u0DD1\\u0DD8-\\u0DDF\\u0DF2\\u0DF3\\u0F3E\\u0F3F\\u0F7F\\u102B\\u102C\\u1031\\u1038\\u103B\\u103C\\u1056\\u1057\\u1062-\\u1064\\u1067-\\u106D\\u1083\\u1084\\u1087-\\u108C\\u108F\\u109A-\\u109C\\u17B6\\u17BE-\\u17C5\\u17C7\\u17C8\\u1923-\\u1926\\u1929-\\u192B\\u1930\\u1931\\u1933-\\u1938\\u19B0-\\u19C0\\u19C8\\u19C9\\u1A19-\\u1A1B\\u1A55\\u1A57\\u1A61\\u1A63\\u1A64\\u1A6D-\\u1A72\\u1B04\\u1B35\\u1B3B\\u1B3D-\\u1B41\\u1B43\\u1B44\\u1B82\\u1BA1\\u1BA6\\u1BA7\\u1BAA\\u1C24-\\u1C2B\\u1C34\\u1C35\\u1CE1\\u1CF2\\uA823\\uA824\\uA827\\uA880\\uA881\\uA8B4-\\uA8C3\\uA952\\uA953\\uA983\\uA9B4\\uA9B5\\uA9BA\\uA9BB\\uA9BD-\\uA9C0\\uAA2F\\uAA30\\uAA33\\uAA34\\uAA4D\\uAA7B\\uABE3\\uABE4\\uABE6\\uABE7\\uABE9\\uABEA\\uABEC]"),
                  connector_punctuation: new RegExp("[\\u005F\\u203F\\u2040\\u2054\\uFE33\\uFE34\\uFE4D-\\uFE4F\\uFF3F]")
          };
          
          function is_letter(ch) {
                  return UNICODE.letter.test(ch);
          };
          
          function is_digit(ch) {
                  ch = ch.charCodeAt(0);
                  return ch >= 48 && ch <= 57; //XXX: find out if "UnicodeDigit" means something else than 0..9
          };
          
          function is_alphanumeric_char(ch) {
                  return is_digit(ch) || is_letter(ch);
          };
          
          function is_unicode_combining_mark(ch) {
                  return UNICODE.non_spacing_mark.test(ch) || UNICODE.space_combining_mark.test(ch);
          };
          
          function is_unicode_connector_punctuation(ch) {
                  return UNICODE.connector_punctuation.test(ch);
          };
          
          function is_identifier_start(ch) {
                  return ch == "$" || ch == "_" || is_letter(ch);
          };
          
          function is_identifier_char(ch) {
                  return is_identifier_start(ch)
                          || is_unicode_combining_mark(ch)
                          || is_digit(ch)
                          || is_unicode_connector_punctuation(ch)
                          || ch == "\u200c" // zero-width non-joiner <ZWNJ>
                          || ch == "\u200d" // zero-width joiner <ZWJ> (in my ECMA-262 PDF, this is also 200c)
                  ;
          };
          
          function parse_js_number(num) {
                  if (RE_HEX_NUMBER.test(num)) {
                          return parseInt(num.substr(2), 16);
                  } else if (RE_OCT_NUMBER.test(num)) {
                          return parseInt(num.substr(1), 8);
                  } else if (RE_DEC_NUMBER.test(num)) {
                          return parseFloat(num);
                  }
          };
          
          function JS_Parse_Error(message, line, col, pos) {
                  this.message = message;
                  this.line = line;
                  this.col = col;
                  this.pos = pos;
                  try {
                          ({})();
                  } catch(ex) {
                          this.stack = ex.stack;
                  };
          };
          
          JS_Parse_Error.prototype.toString = function() {
                  return this.message + " (line: " + this.line + ", col: " + this.col + ", pos: " + this.pos + ")" + "\n\n" + this.stack;
          };
          
          function js_error(message, line, col, pos) {
                  throw new JS_Parse_Error(message, line, col, pos);
          };
          
          function is_token(token, type, val) {
                  return token.type == type && (val == null || token.value == val);
          };
          
          var EX_EOF = {};
          
          function tokenizer($TEXT) {
          
                  var S = {
                          text            : $TEXT.replace(/\r\n?|[\n\u2028\u2029]/g, "\n").replace(/^\uFEFF/, ''),
                          pos             : 0,
                          tokpos          : 0,
                          line            : 0,
                          tokline         : 0,
                          col             : 0,
                          tokcol          : 0,
                          newline_before  : false,
                          regex_allowed   : false,
                          comments_before : []
                  };
          
                  function peek() { return S.text.charAt(S.pos); };
          
                  function next(signal_eof) {
                          var ch = S.text.charAt(S.pos++);
                          if (signal_eof && !ch)
                                  throw EX_EOF;
                          if (ch == "\n") {
                                  S.newline_before = true;
                                  ++S.line;
                                  S.col = 0;
                          } else {
                                  ++S.col;
                          }
                          return ch;
                  };
          
                  function eof() {
                          return !S.peek();
                  };
          
                  function find(what, signal_eof) {
                          var pos = S.text.indexOf(what, S.pos);
                          if (signal_eof && pos == -1) throw EX_EOF;
                          return pos;
                  };
          
                  function start_token() {
                          S.tokline = S.line;
                          S.tokcol = S.col;
                          S.tokpos = S.pos;
                  };
          
                  function token(type, value, is_comment) {
                          S.regex_allowed = ((type == "operator" && !HOP(UNARY_POSTFIX, value)) ||
                                             (type == "keyword" && HOP(KEYWORDS_BEFORE_EXPRESSION, value)) ||
                                             (type == "punc" && HOP(PUNC_BEFORE_EXPRESSION, value)));
                          var ret = {
                                  type  : type,
                                  value : value,
                                  line  : S.tokline,
                                  col   : S.tokcol,
                                  pos   : S.tokpos,
                                  nlb   : S.newline_before
                          };
                          if (!is_comment) {
                                  ret.comments_before = S.comments_before;
                                  S.comments_before = [];
                          }
                          S.newline_before = false;
                          return ret;
                  };
          
                  function skip_whitespace() {
                          while (HOP(WHITESPACE_CHARS, peek()))
                                  next();
                  };
          
                  function read_while(pred) {
                          var ret = "", ch = peek(), i = 0;
                          while (ch && pred(ch, i++)) {
                                  ret += next();
                                  ch = peek();
                          }
                          return ret;
                  };
          
                  function parse_error(err) {
                          js_error(err, S.tokline, S.tokcol, S.tokpos);
                  };
          
                  function read_num(prefix) {
                          var has_e = false, after_e = false, has_x = false, has_dot = prefix == ".";
                          var num = read_while(function(ch, i){
                                  if (ch == "x" || ch == "X") {
                                          if (has_x) return false;
                                          return has_x = true;
                                  }
                                  if (!has_x && (ch == "E" || ch == "e")) {
                                          if (has_e) return false;
                                          return has_e = after_e = true;
                                  }
                                  if (ch == "-") {
                                          if (after_e || (i == 0 && !prefix)) return true;
                                          return false;
                                  }
                                  if (ch == "+") return after_e;
                                  after_e = false;
                                  if (ch == ".") {
                                          if (!has_dot && !has_x)
                                                  return has_dot = true;
                                          return false;
                                  }
                                  return is_alphanumeric_char(ch);
                          });
                          if (prefix)
                                  num = prefix + num;
                          var valid = parse_js_number(num);
                          if (!isNaN(valid)) {
                                  return token("num", valid);
                          } else {
                                  parse_error("Invalid syntax: " + num);
                          }
                  };
          
                  function read_escaped_char() {
                          var ch = next(true);
                          switch (ch) {
                              case "n" : return "\n";
                              case "r" : return "\r";
                              case "t" : return "\t";
                              case "b" : return "\b";
                              case "v" : return "\v";
                              case "f" : return "\f";
                              case "0" : return "\0";
                              case "x" : return String.fromCharCode(hex_bytes(2));
                              case "u" : return String.fromCharCode(hex_bytes(4));
                              default  : return ch;
                          }
                  };
          
                  function hex_bytes(n) {
                          var num = 0;
                          for (; n > 0; --n) {
                                  var digit = parseInt(next(true), 16);
                                  if (isNaN(digit))
                                          parse_error("Invalid hex-character pattern in string");
                                  num = (num << 4) | digit;
                          }
                          return num;
                  };
          
                  function read_string() {
                          return with_eof_error("Unterminated string constant", function(){
                                  var quote = next(), ret = "";
                                  for (;;) {
                                          var ch = next(true);
                                          if (ch == "\\") ch = read_escaped_char();
                                          else if (ch == quote) break;
                                          ret += ch;
                                  }
                                  return token("string", ret);
                          });
                  };
          
                  function read_line_comment() {
                          next();
                          var i = find("\n"), ret;
                          if (i == -1) {
                                  ret = S.text.substr(S.pos);
                                  S.pos = S.text.length;
                          } else {
                                  ret = S.text.substring(S.pos, i);
                                  S.pos = i;
                          }
                          return token("comment1", ret, true);
                  };
          
                  function read_multiline_comment() {
                          next();
                          return with_eof_error("Unterminated multiline comment", function(){
                                  var i = find("*/", true),
                                      text = S.text.substring(S.pos, i),
                                      tok = token("comment2", text, true);
                                  S.pos = i + 2;
                                  S.line += text.split("\n").length - 1;
                                  S.newline_before = text.indexOf("\n") >= 0;
          
                                  // https://github.com/mishoo/UglifyJS/issues/#issue/100
                                  if (/^@cc_on/i.test(text)) {
                                          warn("WARNING: at line " + S.line);
                                          warn("*** Found \"conditional comment\": " + text);
                                          warn("*** UglifyJS DISCARDS ALL COMMENTS.  This means your code might no longer work properly in Internet Explorer.");
                                  }
          
                                  return tok;
                          });
                  };
          
                  function read_name() {
                          var backslash = false, name = "", ch;
                          while ((ch = peek()) != null) {
                                  if (!backslash) {
                                          if (ch == "\\") backslash = true, next();
                                          else if (is_identifier_char(ch)) name += next();
                                          else break;
                                  }
                                  else {
                                          if (ch != "u") parse_error("Expecting UnicodeEscapeSequence -- uXXXX");
                                          ch = read_escaped_char();
                                          if (!is_identifier_char(ch)) parse_error("Unicode char: " + ch.charCodeAt(0) + " is not valid in identifier");
                                          name += ch;
                                          backslash = false;
                                  }
                          }
                          return name;
                  };
          
                  function read_regexp() {
                          return with_eof_error("Unterminated regular expression", function(){
                                  var prev_backslash = false, regexp = "", ch, in_class = false;
                                  while ((ch = next(true))) if (prev_backslash) {
                                          regexp += "\\" + ch;
                                          prev_backslash = false;
                                  } else if (ch == "[") {
                                          in_class = true;
                                          regexp += ch;
                                  } else if (ch == "]" && in_class) {
                                          in_class = false;
                                          regexp += ch;
                                  } else if (ch == "/" && !in_class) {
                                          break;
                                  } else if (ch == "\\") {
                                          prev_backslash = true;
                                  } else {
                                          regexp += ch;
                                  }
                                  var mods = read_name();
                                  return token("regexp", [ regexp, mods ]);
                          });
                  };
          
                  function read_operator(prefix) {
                          function grow(op) {
                                  if (!peek()) return op;
                                  var bigger = op + peek();
                                  if (HOP(OPERATORS, bigger)) {
                                          next();
                                          return grow(bigger);
                                  } else {
                                          return op;
                                  }
                          };
                          return token("operator", grow(prefix || next()));
                  };
          
                  function handle_slash() {
                          next();
                          var regex_allowed = S.regex_allowed;
                          switch (peek()) {
                              case "/":
                                  S.comments_before.push(read_line_comment());
                                  S.regex_allowed = regex_allowed;
                                  return next_token();
                              case "*":
                                  S.comments_before.push(read_multiline_comment());
                                  S.regex_allowed = regex_allowed;
                                  return next_token();
                          }
                          return S.regex_allowed ? read_regexp() : read_operator("/");
                  };
          
                  function handle_dot() {
                          next();
                          return is_digit(peek())
                                  ? read_num(".")
                                  : token("punc", ".");
                  };
          
                  function read_word() {
                          var word = read_name();
                          return !HOP(KEYWORDS, word)
                                  ? token("name", word)
                                  : HOP(OPERATORS, word)
                                  ? token("operator", word)
                                  : HOP(KEYWORDS_ATOM, word)
                                  ? token("atom", word)
                                  : token("keyword", word);
                  };
          
                  function with_eof_error(eof_error, cont) {
                          try {
                                  return cont();
                          } catch(ex) {
                                  if (ex === EX_EOF) parse_error(eof_error);
                                  else throw ex;
                          }
                  };
          
                  function next_token(force_regexp) {
                          if (force_regexp)
                                  return read_regexp();
                          skip_whitespace();
                          start_token();
                          var ch = peek();
                          if (!ch) return token("eof");
                          if (is_digit(ch)) return read_num();
                          if (ch == '"' || ch == "'") return read_string();
                          if (HOP(PUNC_CHARS, ch)) return token("punc", next());
                          if (ch == ".") return handle_dot();
                          if (ch == "/") return handle_slash();
                          if (HOP(OPERATOR_CHARS, ch)) return read_operator();
                          if (ch == "\\" || is_identifier_start(ch)) return read_word();
                          parse_error("Unexpected character '" + ch + "'");
                  };
          
                  next_token.context = function(nc) {
                          if (nc) S = nc;
                          return S;
                  };
          
                  return next_token;
          
          };
          
          /* -----[ Parser (constants) ]----- */
          
          var UNARY_PREFIX = array_to_hash([
                  "typeof",
                  "void",
                  "delete",
                  "--",
                  "++",
                  "!",
                  "~",
                  "-",
                  "+"
          ]);
          
          var UNARY_POSTFIX = array_to_hash([ "--", "++" ]);
          
          var ASSIGNMENT = (function(a, ret, i){
                  while (i < a.length) {
                          ret[a[i]] = a[i].substr(0, a[i].length - 1);
                          i++;
                  }
                  return ret;
          })(
                  ["+=", "-=", "/=", "*=", "%=", ">>=", "<<=", ">>>=", "|=", "^=", "&="],
                  { "=": true },
                  0
          );
          
          var PRECEDENCE = (function(a, ret){
                  for (var i = 0, n = 1; i < a.length; ++i, ++n) {
                          var b = a[i];
                          for (var j = 0; j < b.length; ++j) {
                                  ret[b[j]] = n;
                          }
                  }
                  return ret;
          })(
                  [
                          ["||"],
                          ["&&"],
                          ["|"],
                          ["^"],
                          ["&"],
                          ["==", "===", "!=", "!=="],
                          ["<", ">", "<=", ">=", "in", "instanceof"],
                          [">>", "<<", ">>>"],
                          ["+", "-"],
                          ["*", "/", "%"]
                  ],
                  {}
          );
          
          var STATEMENTS_WITH_LABELS = array_to_hash([ "for", "do", "while", "switch" ]);
          
          var ATOMIC_START_TOKEN = array_to_hash([ "atom", "num", "string", "regexp", "name" ]);
          
          /* -----[ Parser ]----- */
          
          function NodeWithToken(str, start, end) {
                  this.name = str;
                  this.start = start;
                  this.end = end;
          };
          
          NodeWithToken.prototype.toString = function() { return this.name; };
          
          function parse($TEXT, exigent_mode, embed_tokens) {
          
                  var S = {
                          input       : typeof $TEXT == "string" ? tokenizer($TEXT, true) : $TEXT,
                          token       : null,
                          prev        : null,
                          peeked      : null,
                          in_function : 0,
                          in_loop     : 0,
                          labels      : []
                  };
          
                  S.token = next();
          
                  function is(type, value) {
                          return is_token(S.token, type, value);
                  };
          
                  function peek() { return S.peeked || (S.peeked = S.input()); };
          
                  function next() {
                          S.prev = S.token;
                          if (S.peeked) {
                                  S.token = S.peeked;
                                  S.peeked = null;
                          } else {
                                  S.token = S.input();
                          }
                          return S.token;
                  };
          
                  function prev() {
                          return S.prev;
                  };
          
                  function croak(msg, line, col, pos) {
                          var ctx = S.input.context();
                          js_error(msg,
                                   line != null ? line : ctx.tokline,
                                   col != null ? col : ctx.tokcol,
                                   pos != null ? pos : ctx.tokpos);
                  };
          
                  function token_error(token, msg) {
                          croak(msg, token.line, token.col);
                  };
          
                  function unexpected(token) {
                          if (token == null)
                                  token = S.token;
                          token_error(token, "Unexpected token: " + token.type + " (" + token.value + ")");
                  };
          
                  function expect_token(type, val) {
                          if (is(type, val)) {
                                  return next();
                          }
                          token_error(S.token, "Unexpected token " + S.token.type + ", expected " + type);
                  };
          
                  function expect(punc) { return expect_token("punc", punc); };
          
                  function can_insert_semicolon() {
                          return !exigent_mode && (
                                  S.token.nlb || is("eof") || is("punc", "}")
                          );
                  };
          
                  function semicolon() {
                          if (is("punc", ";")) next();
                          else if (!can_insert_semicolon()) unexpected();
                  };
          
                  function as() {
                          return slice(arguments);
                  };
          
                  function parenthesised() {
                          expect("(");
                          var ex = expression();
                          expect(")");
                          return ex;
                  };
          
                  function add_tokens(str, start, end) {
                          return str instanceof NodeWithToken ? str : new NodeWithToken(str, start, end);
                  };
          
                  var statement = embed_tokens ? function() {
                          var start = S.token;
                          var ast = $statement.apply(this, arguments);
                          ast[0] = add_tokens(ast[0], start, prev());
                          return ast;
                  } : $statement;
          
                  function $statement() {
                          if (is("operator", "/")) {
                                  S.peeked = null;
                                  S.token = S.input(true); // force regexp
                          }
                          switch (S.token.type) {
                              case "num":
                              case "string":
                              case "regexp":
                              case "operator":
                              case "atom":
                                  return simple_statement();
          
                              case "name":
                                  return is_token(peek(), "punc", ":")
                                          ? labeled_statement(prog1(S.token.value, next, next))
                                          : simple_statement();
          
                              case "punc":
                                  switch (S.token.value) {
                                      case "{":
                                          return as("block", block_());
                                      case "[":
                                      case "(":
                                          return simple_statement();
                                      case ";":
                                          next();
                                          return as("block");
                                      default:
                                          unexpected();
                                  }
          
                              case "keyword":
                                  switch (prog1(S.token.value, next)) {
                                      case "break":
                                          return break_cont("break");
          
                                      case "continue":
                                          return break_cont("continue");
          
                                      case "debugger":
                                          semicolon();
                                          return as("debugger");
          
                                      case "do":
                                          return (function(body){
                                                  expect_token("keyword", "while");
                                                  return as("do", prog1(parenthesised, semicolon), body);
                                          })(in_loop(statement));
          
                                      case "for":
                                          return for_();
          
                                      case "function":
                                          return function_(true);
          
                                      case "if":
                                          return if_();
          
                                      case "return":
                                          if (S.in_function == 0)
                                                  croak("'return' outside of function");
                                          return as("return",
                                                    is("punc", ";")
                                                    ? (next(), null)
                                                    : can_insert_semicolon()
                                                    ? null
                                                    : prog1(expression, semicolon));
          
                                      case "switch":
                                          return as("switch", parenthesised(), switch_block_());
          
                                      case "throw":
                                          return as("throw", prog1(expression, semicolon));
          
                                      case "try":
                                          return try_();
          
                                      case "var":
                                          return prog1(var_, semicolon);
          
                                      case "const":
                                          return prog1(const_, semicolon);
          
                                      case "while":
                                          return as("while", parenthesised(), in_loop(statement));
          
                                      case "with":
                                          return as("with", parenthesised(), statement());
          
                                      default:
                                          unexpected();
                                  }
                          }
                  };
          
                  function labeled_statement(label) {
                          S.labels.push(label);
                          var start = S.token, stat = statement();
                          if (exigent_mode && !HOP(STATEMENTS_WITH_LABELS, stat[0]))
                                  unexpected(start);
                          S.labels.pop();
                          return as("label", label, stat);
                  };
          
                  function simple_statement() {
                          return as("stat", prog1(expression, semicolon));
                  };
          
                  function break_cont(type) {
                          var name = is("name") ? S.token.value : null;
                          if (name != null) {
                                  next();
                                  if (!member(name, S.labels))
                                          croak("Label " + name + " without matching loop or statement");
                          }
                          else if (S.in_loop == 0)
                                  croak(type + " not inside a loop or switch");
                          semicolon();
                          return as(type, name);
                  };
          
                  function for_() {
                          expect("(");
                          var init = null;
                          if (!is("punc", ";")) {
                                  init = is("keyword", "var")
                                          ? (next(), var_(true))
                                          : expression(true, true);
                                  if (is("operator", "in"))
                                          return for_in(init);
                          }
                          return regular_for(init);
                  };
          
                  function regular_for(init) {
                          expect(";");
                          var test = is("punc", ";") ? null : expression();
                          expect(";");
                          var step = is("punc", ")") ? null : expression();
                          expect(")");
                          return as("for", init, test, step, in_loop(statement));
                  };
          
                  function for_in(init) {
                          var lhs = init[0] == "var" ? as("name", init[1][0]) : init;
                          next();
                          var obj = expression();
                          expect(")");
                          return as("for-in", init, lhs, obj, in_loop(statement));
                  };
          
                  var function_ = embed_tokens ? function() {
                          var start = prev();
                          var ast = $function_.apply(this, arguments);
                          ast[0] = add_tokens(ast[0], start, prev());
                          return ast;
                  } : $function_;
          
                  function $function_(in_statement) {
                          var name = is("name") ? prog1(S.token.value, next) : null;
                          if (in_statement && !name)
                                  unexpected();
                          expect("(");
                          return as(in_statement ? "defun" : "function",
                                    name,
                                    // arguments
                                    (function(first, a){
                                            while (!is("punc", ")")) {
                                                    if (first) first = false; else expect(",");
                                                    if (!is("name")) unexpected();
                                                    a.push(S.token.value);
                                                    next();
                                            }
                                            next();
                                            return a;
                                    })(true, []),
                                    // body
                                    (function(){
                                            ++S.in_function;
                                            var loop = S.in_loop;
                                            S.in_loop = 0;
                                            var a = block_();
                                            --S.in_function;
                                            S.in_loop = loop;
                                            return a;
                                    })());
                  };
          
                  function if_() {
                          var cond = parenthesised(), body = statement(), belse;
                          if (is("keyword", "else")) {
                                  next();
                                  belse = statement();
                          }
                          return as("if", cond, body, belse);
                  };
          
                  function block_() {
                          expect("{");
                          var a = [];
                          while (!is("punc", "}")) {
                                  if (is("eof")) unexpected();
                                  a.push(statement());
                          }
                          next();
                          return a;
                  };
          
                  var switch_block_ = curry(in_loop, function(){
                          expect("{");
                          var a = [], cur = null;
                          while (!is("punc", "}")) {
                                  if (is("eof")) unexpected();
                                  if (is("keyword", "case")) {
                                          next();
                                          cur = [];
                                          a.push([ expression(), cur ]);
                                          expect(":");
                                  }
                                  else if (is("keyword", "default")) {
                                          next();
                                          expect(":");
                                          cur = [];
                                          a.push([ null, cur ]);
                                  }
                                  else {
                                          if (!cur) unexpected();
                                          cur.push(statement());
                                  }
                          }
                          next();
                          return a;
                  });
          
                  function try_() {
                          var body = block_(), bcatch, bfinally;
                          if (is("keyword", "catch")) {
                                  next();
                                  expect("(");
                                  if (!is("name"))
                                          croak("Name expected");
                                  var name = S.token.value;
                                  next();
                                  expect(")");
                                  bcatch = [ name, block_() ];
                          }
                          if (is("keyword", "finally")) {
                                  next();
                                  bfinally = block_();
                          }
                          if (!bcatch && !bfinally)
                                  croak("Missing catch/finally blocks");
                          return as("try", body, bcatch, bfinally);
                  };
          
                  function vardefs(no_in) {
                          var a = [];
                          for (;;) {
                                  if (!is("name"))
                                          unexpected();
                                  var name = S.token.value;
                                  next();
                                  if (is("operator", "=")) {
                                          next();
                                          a.push([ name, expression(false, no_in) ]);
                                  } else {
                                          a.push([ name ]);
                                  }
                                  if (!is("punc", ","))
                                          break;
                                  next();
                          }
                          return a;
                  };
          
                  function var_(no_in) {
                          return as("var", vardefs(no_in));
                  };
          
                  function const_() {
                          return as("const", vardefs());
                  };
          
                  function new_() {
                          var newexp = expr_atom(false), args;
                          if (is("punc", "(")) {
                                  next();
                                  args = expr_list(")");
                          } else {
                                  args = [];
                          }
                          return subscripts(as("new", newexp, args), true);
                  };
          
                  function expr_atom(allow_calls) {
                          if (is("operator", "new")) {
                                  next();
                                  return new_();
                          }
                          if (is("operator") && HOP(UNARY_PREFIX, S.token.value)) {
                                  return make_unary("unary-prefix",
                                                    prog1(S.token.value, next),
                                                    expr_atom(allow_calls));
                          }
                          if (is("punc")) {
                                  switch (S.token.value) {
                                      case "(":
                                          next();
                                          return subscripts(prog1(expression, curry(expect, ")")), allow_calls);
                                      case "[":
                                          next();
                                          return subscripts(array_(), allow_calls);
                                      case "{":
                                          next();
                                          return subscripts(object_(), allow_calls);
                                  }
                                  unexpected();
                          }
                          if (is("keyword", "function")) {
                                  next();
                                  return subscripts(function_(false), allow_calls);
                          }
                          if (HOP(ATOMIC_START_TOKEN, S.token.type)) {
                                  var atom = S.token.type == "regexp"
                                          ? as("regexp", S.token.value[0], S.token.value[1])
                                          : as(S.token.type, S.token.value);
                                  return subscripts(prog1(atom, next), allow_calls);
                          }
                          unexpected();
                  };
          
                  function expr_list(closing, allow_trailing_comma, allow_empty) {
                          var first = true, a = [];
                          while (!is("punc", closing)) {
                                  if (first) first = false; else expect(",");
                                  if (allow_trailing_comma && is("punc", closing)) break;
                                  if (is("punc", ",") && allow_empty) {
                                          a.push([ "atom", "undefined" ]);
                                  } else {
                                          a.push(expression(false));
                                  }
                          }
                          next();
                          return a;
                  };
          
                  function array_() {
                          return as("array", expr_list("]", !exigent_mode, true));
                  };
          
                  function object_() {
                          var first = true, a = [];
                          while (!is("punc", "}")) {
                                  if (first) first = false; else expect(",");
                                  if (!exigent_mode && is("punc", "}"))
                                          // allow trailing comma
                                          break;
                                  var type = S.token.type;
                                  var name = as_property_name();
                                  if (type == "name" && (name == "get" || name == "set") && !is("punc", ":")) {
                                          a.push([ as_name(), function_(false), name ]);
                                  } else {
                                          expect(":");
                                          a.push([ name, expression(false) ]);
                                  }
                          }
                          next();
                          return as("object", a);
                  };
          
                  function as_property_name() {
                          switch (S.token.type) {
                              case "num":
                              case "string":
                                  return prog1(S.token.value, next);
                          }
                          return as_name();
                  };
          
                  function as_name() {
                          switch (S.token.type) {
                              case "name":
                              case "operator":
                              case "keyword":
                              case "atom":
                                  return prog1(S.token.value, next);
                              default:
                                  unexpected();
                          }
                  };
          
                  function subscripts(expr, allow_calls) {
                          if (is("punc", ".")) {
                                  next();
                                  return subscripts(as("dot", expr, as_name()), allow_calls);
                          }
                          if (is("punc", "[")) {
                                  next();
                                  return subscripts(as("sub", expr, prog1(expression, curry(expect, "]"))), allow_calls);
                          }
                          if (allow_calls && is("punc", "(")) {
                                  next();
                                  return subscripts(as("call", expr, expr_list(")")), true);
                          }
                          if (allow_calls && is("operator") && HOP(UNARY_POSTFIX, S.token.value)) {
                                  return prog1(curry(make_unary, "unary-postfix", S.token.value, expr),
                                               next);
                          }
                          return expr;
                  };
          
                  function make_unary(tag, op, expr) {
                          if ((op == "++" || op == "--") && !is_assignable(expr))
                                  croak("Invalid use of " + op + " operator");
                          return as(tag, op, expr);
                  };
          
                  function expr_op(left, min_prec, no_in) {
                          var op = is("operator") ? S.token.value : null;
                          if (op && op == "in" && no_in) op = null;
                          var prec = op != null ? PRECEDENCE[op] : null;
                          if (prec != null && prec > min_prec) {
                                  next();
                                  var right = expr_op(expr_atom(true), prec, no_in);
                                  return expr_op(as("binary", op, left, right), min_prec, no_in);
                          }
                          return left;
                  };
          
                  function expr_ops(no_in) {
                          return expr_op(expr_atom(true), 0, no_in);
                  };
          
                  function maybe_conditional(no_in) {
                          var expr = expr_ops(no_in);
                          if (is("operator", "?")) {
                                  next();
                                  var yes = expression(false);
                                  expect(":");
                                  return as("conditional", expr, yes, expression(false, no_in));
                          }
                          return expr;
                  };
          
                  function is_assignable(expr) {
                          if (!exigent_mode) return true;
                          switch (expr[0]) {
                              case "dot":
                              case "sub":
                              case "new":
                              case "call":
                                  return true;
                              case "name":
                                  return expr[1] != "this";
                          }
                  };
          
                  function maybe_assign(no_in) {
                          var left = maybe_conditional(no_in), val = S.token.value;
                          if (is("operator") && HOP(ASSIGNMENT, val)) {
                                  if (is_assignable(left)) {
                                          next();
                                          return as("assign", ASSIGNMENT[val], left, maybe_assign(no_in));
                                  }
                                  croak("Invalid assignment");
                          }
                          return left;
                  };
          
                  function expression(commas, no_in) {
                          if (arguments.length == 0)
                                  commas = true;
                          var expr = maybe_assign(no_in);
                          if (commas && is("punc", ",")) {
                                  next();
                                  return as("seq", expr, expression(true, no_in));
                          }
                          return expr;
                  };
          
                  function in_loop(cont) {
                          try {
                                  ++S.in_loop;
                                  return cont();
                          } finally {
                                  --S.in_loop;
                          }
                  };
          
                  return as("toplevel", (function(a){
                          while (!is("eof"))
                                  a.push(statement());
                          return a;
                  })([]));
          
          };
          
          /* -----[ Utilities ]----- */
          
          function curry(f) {
                  var args = slice(arguments, 1);
                  return function() { return f.apply(this, args.concat(slice(arguments))); };
          };
          
          function prog1(ret) {
                  if (ret instanceof Function)
                          ret = ret();
                  for (var i = 1, n = arguments.length; --n > 0; ++i)
                          arguments[i]();
                  return ret;
          };
          
          function array_to_hash(a) {
                  var ret = {};
                  for (var i = 0; i < a.length; ++i)
                          ret[a[i]] = true;
                  return ret;
          };
          
          function slice(a, start) {
                  return Array.prototype.slice.call(a, start == null ? 0 : start);
          };
          
          function characters(str) {
                  return str.split("");
          };
          
          function member(name, array) {
                  for (var i = array.length; --i >= 0;)
                          if (array[i] === name)
                                  return true;
                  return false;
          };
          
          function HOP(obj, prop) {
                  return Object.prototype.hasOwnProperty.call(obj, prop);
          };
          
          var warn = function() {};
          
          /* -----[ Exports ]----- */
          
          var init = function (root) {
              if (root.modules["parser"]) {
                  return;
              }
              
              root.parse = parse;
              
              root.modules["parser"] = true;
          }
          
          var isCommonJS = (typeof require !== "undefined" && typeof module !== "undefined" && module.exports);
          var isAmd = (typeof define !== "undefined" && define.amd);
          
          if (isCommonJS) {
              module.exports.init = init;
          } else if (isAmd) {
              define("jscex-parser", function () {
                  return { init: init };
              });
          } else {
              if (typeof Jscex === "undefined") {
                  throw new Error('Missing root object, please load "jscex" module first.');
              }
              
              init(Jscex);
          }
          
          /*
          scope.tokenizer = tokenizer;
          scope.parse = parse;
          scope.slice = slice;
          scope.curry = curry;
          scope.member = member;
          scope.array_to_hash = array_to_hash;
          scope.PRECEDENCE = PRECEDENCE;
          scope.KEYWORDS_ATOM = KEYWORDS_ATOM;
          scope.RESERVED_WORDS = RESERVED_WORDS;
          scope.KEYWORDS = KEYWORDS;
          scope.ATOMIC_START_TOKEN = ATOMIC_START_TOKEN;
          scope.OPERATORS = OPERATORS;
          scope.is_alphanumeric_char = is_alphanumeric_char;
          scope.set_logger = function (logger) {
              warn = logger;
          };
          */
          
          })();</script>
		<script>(function () {
    
            var codeGenerator = (typeof eval("(function () {})") == "function") ?
                function (code) { return code; } :
                function (code) { return "false || " + code; };
                
            // support string type only.
            var stringify = (typeof JSON !== "undefined" && JSON.stringify) ?
                function (s) { return JSON.stringify(s); } :
                (function () {
                    // Implementation comes from JSON2 (http://www.json.org/js.html)
                
                    var escapable = /[\\\"\x00-\x1f\x7f-\x9f\u00ad\u0600-\u0604\u070f\u17b4\u17b5\u200c-\u200f\u2028-\u202f\u2060-\u206f\ufeff\ufff0-\uffff]/g;
                    
                    var meta = {    // table of character substitutions
                        '\b': '\\b',
                        '\t': '\\t',
                        '\n': '\\n',
                        '\f': '\\f',
                        '\r': '\\r',
                        '"' : '\\"',
                        '\\': '\\\\'
                    }
                    
                    return function (s) {
                        // If the string contains no control characters, no quote characters, and no
                        // backslash characters, then we can safely slap some quotes around it.
                        // Otherwise we must also replace the offending characters with safe escape
                        // sequences.
        
                        escapable.lastIndex = 0;
                        return escapable.test(s) ? '"' + s.replace(escapable, function (a) {
                            var c = meta[a];
                            return typeof c === 's' ? c :
                                '\\u' + ('0000' + a.charCodeAt(0).toString(16)).slice(-4);
                        }) + '"' : '"' + s + '"';
                    };
                })();
            
            // seed defined in global
            if (typeof __jscex__tempVarSeed === "undefined") {
                __jscex__tempVarSeed = 0;
            }
        
            var init = function (root) {
            
                if (root.modules["jit"]) {
                    return;
                }
            
                function JscexTreeGenerator(binder) {
                    this._binder = binder;
                    this._root = null;
                }
                JscexTreeGenerator.prototype = {
        
                    generate: function (ast) {
        
                        var params = ast[2], statements = ast[3];
        
                        this._root = { type: "delay", stmts: [] };
        
                        this._visitStatements(statements, this._root.stmts);
        
                        return this._root;
                    },
        
                    _getBindInfo: function (stmt) {
        
                        var type = stmt[0];
                        if (type == "stat") {
                            var expr = stmt[1];
                            if (expr[0] == "call") {
                                var callee = expr[1];
                                if (callee[0] == "name" && callee[1] == this._binder && expr[2].length == 1) {
                                    return {
                                        expression: expr[2][0],
                                        argName: "",
                                        assignee: null
                                    };
                                }
                            } else if (expr[0] == "assign") {
                                var assignee = expr[2];
                                expr = expr[3];
                                if (expr[0] == "call") {
                                    var callee = expr[1];
                                    if (callee[0] == "name" && callee[1] == this._binder && expr[2].length == 1) {
                                        return {
                                            expression: expr[2][0],
                                            argName: "$$_result_$$",
                                            assignee: assignee
                                        };
                                    }
                                }
                            }
                        } else if (type == "var") {
                            var defs = stmt[1];
                            if (defs.length == 1) {
                                var item = defs[0];
                                var name = item[0];
                                var expr = item[1];
                                if (expr && expr[0] == "call") {
                                    var callee = expr[1];
                                    if (callee[0] == "name" && callee[1] == this._binder && expr[2].length == 1) {
                                        return {
                                            expression: expr[2][0],
                                            argName: name,
                                            assignee: null
                                        };                            
                                    }
                                }
                            }
                        } else if (type == "return") {
                            var expr = stmt[1];
                            if (expr && expr[0] == "call") {
                                var callee = expr[1];
                                if (callee[0] == "name" && callee[1] == this._binder && expr[2].length == 1) {
                                    return {
                                        expression: expr[2][0],
                                        argName: "$$_result_$$",
                                        assignee: "return"
                                    };
                                }
                            }
                        }
        
                        return null;
                    },
        
                    _visitStatements: function (statements, stmts, index) {
                        if (arguments.length <= 2) index = 0;
        
                        if (index >= statements.length) {
                            stmts.push({ type: "normal" });
                            return this;
                        }
        
                        var currStmt = statements[index];
                        var bindInfo = this._getBindInfo(currStmt);
        
                        if (bindInfo) {
                            var bindStmt = { type: "bind", info: bindInfo };
                            stmts.push(bindStmt);
        
                            if (bindInfo.assignee != "return") {
                                bindStmt.stmts = [];
                                this._visitStatements(statements, bindStmt.stmts, index + 1);
                            }
        
                        } else {
                            var type = currStmt[0];
                            if (type == "return" || type == "break" || type == "continue" || type == "throw") {
        
                                stmts.push({ type: type, stmt: currStmt });
        
                            } else if (type == "if" || type == "try" || type == "for" || type == "do"
                                       || type == "while" || type == "switch" || type == "for-in") {
        
                                var newStmt = this._visit(currStmt);
        
                                if (newStmt.type == "raw") {
                                    stmts.push(newStmt);
                                    this._visitStatements(statements, stmts, index + 1);
                                } else {
                                    var isLast = (index == statements.length - 1);
                                    if (isLast) {
                                        stmts.push(newStmt);
                                    } else {
        
                                        var combineStmt = {
                                            type: "combine",
                                            first: { type: "delay", stmts: [newStmt] },
                                            second: { type: "delay", stmts: [] }
                                        };
                                        stmts.push(combineStmt);
        
                                        this._visitStatements(statements, combineStmt.second.stmts, index + 1);
                                    }
                                }
        
                            } else {
        
                                stmts.push({ type: "raw", stmt: currStmt });
        
                                this._visitStatements(statements, stmts, index + 1);
                            }
                        }
        
                        return this;
                    },
        
                    _visit: function (ast) {
        
                        var type = ast[0];
        
                        function throwUnsupportedError() {
                            throw new Error('"' + type + '" is not currently supported.');
                        }
        
                        var visitor = this._visitors[type];
        
                        if (visitor) {
                            return visitor.call(this, ast);
                        } else {
                            throwUnsupportedError();
                        }
                    },
        
                    _visitBody: function (ast, stmts) {
                        if (ast[0] == "block") {
                            this._visitStatements(ast[1], stmts);
                        } else {
                            this._visitStatements([ast], stmts);
                        }
                    },
        
                    _noBinding: function (stmts) {
                        switch (stmts[stmts.length - 1].type) {
                            case "normal":
                            case "return":
                            case "break":
                            case "throw":
                            case "continue":
                                return true;
                        }
        
                        return false;
                    },
        
                    _collectCaseStatements: function (cases, index) {
                        var res = [];
        
                        for (var i = index; i < cases.length; i++) {
                            var rawStmts = cases[i][1];
                            for (var j = 0; j < rawStmts.length; j++) {
                                if (rawStmts[j][0] == "break") {
                                    return res
                                }
        
                                res.push(rawStmts[j]);
                            }
                        }
        
                        return res;
                    },
        
                    _visitors: {
        
                        "for": function (ast) {
        
                            var bodyStmts = [];
                            var body = ast[4];
                            this._visitBody(body, bodyStmts);
        
                            if (this._noBinding(bodyStmts)) {
                                return { type: "raw", stmt: ast };
                            }
        
                            var delayStmt = { type: "delay", stmts: [] };
                    
                            var setup = ast[1];
                            if (setup) {
                                delayStmt.stmts.push({ type: "raw", stmt: setup });
                            }
        
                            var loopStmt = { type: "loop", bodyFirst: false, bodyStmt: { type: "delay", stmts: bodyStmts } };
                            delayStmt.stmts.push(loopStmt);
                            
                            var condition = ast[2];
                            if (condition) {
                                loopStmt.condition = condition;
                            }
                            
                            var update = ast[3];
                            if (update) {
                                loopStmt.update = update;
                            }
        
                            return delayStmt;
                        },
        
                        "for-in": function (ast) {
        
                            var body = ast[4];
                            
                            var bodyStmts = [];
                            this._visitBody(body, bodyStmts);
        
                            if (this._noBinding(bodyStmts)) {
                                return { type: "raw", stmt: ast };
                            }
                        
                            var id = (__jscex__tempVarSeed++);
                            var keysVar = "$$_keys_$$_" + id;
                            var indexVar = "$$_index_$$_" + id;
                            // var memVar = "$$_mem_$$_" + id;
        
                            var delayStmt = { type: "delay", stmts: [] };
        
                            // var members = Jscex._forInKeys(obj);
                            var keysAst = root.parse("var " + keysVar + " = Jscex._forInKeys(obj);")[1][0];
                            keysAst[1][0][1][2][0] = ast[3]; // replace obj with real AST;
                            delayStmt.stmts.push({ type: "raw", stmt: keysAst });
        
                            /*
                            // var members = [];
                            delayStmt.stmts.push({
                                type: "raw",
                                stmt: uglifyJS.parse("var " + membersVar + " = [];")[1][0]
                            });
                            
                            // for (var mem in obj) members.push(mem);
                            var keysAst = uglifyJS.parse("for (var " + memVar +" in obj) " + membersVar + ".push(" + memVar + ");")[1][0];
                            keysAst[3] = ast[3]; // replace the "obj" with real AST.
                            delayStmt.stmts.push({ type : "raw", stmt: keysAst});
                            */
                            
                            // var index = 0;
                            delayStmt.stmts.push({
                                type: "raw",
                                stmt: root.parse("var " + indexVar + " = 0;")[1][0]
                            });
        
                            // index < members.length
                            var condition = root.parse(indexVar + " < " + keysVar + ".length")[1][0][1];
        
                            // index++
                            var update = root.parse(indexVar + "++")[1][0][1];
        
                            var loopStmt = {
                                type: "loop",
                                bodyFirst: false,
                                update: update,
                                condition: condition,
                                bodyStmt: { type: "delay", stmts: [] }
                            };
                            delayStmt.stmts.push(loopStmt);
        
                            var varName = ast[2][1]; // ast[2] == ["name", m]
                            if (ast[1][0] == "var") {
                                loopStmt.bodyStmt.stmts.push({
                                    type: "raw",
                                    stmt: root.parse("var " + varName + " = " + keysVar + "[" + indexVar + "];")[1][0]
                                });
                            } else {
                                loopStmt.bodyStmt.stmts.push({
                                    type: "raw",
                                    stmt: root.parse(varName + " = " + keysVar + "[" + indexVar + "];")[1][0]
                                });
                            }
        
                            this._visitBody(body, loopStmt.bodyStmt.stmts);
        
                            return delayStmt;
                        },
        
                        "while": function (ast) {
        
                            var bodyStmts = [];
                            var body = ast[2];
                            this._visitBody(body, bodyStmts);
        
                            if (this._noBinding(bodyStmts)) {
                                return { type: "raw", stmt: ast }
                            }
        
                            var loopStmt = { type: "loop", bodyFirst: false, bodyStmt: { type: "delay", stmts: bodyStmts } };
        
                            var condition = ast[1];
                            loopStmt.condition = condition;
        
                            return loopStmt;
                        },
        
                        "do": function (ast) {
        
                            var bodyStmts = [];
                            var body = ast[2];
                            this._visitBody(body, bodyStmts);
        
                            if (this._noBinding(bodyStmts)) {
                                return { type: "raw", stmt: ast };
                            }
        
                            var loopStmt = { type: "loop", bodyFirst: true, bodyStmt: { type: "delay", stmts: bodyStmts } };
        
                            var condition = ast[1];
                            loopStmt.condition = condition;
        
                            return loopStmt;
                        },
        
                        "switch": function (ast) {
                            var noBinding = true;
        
                            var switchStmt = { type: "switch", item: ast[1], caseStmts: [] };
        
                            var cases = ast[2];
                            for (var i = 0; i < cases.length; i++) {                    
                                var caseStmt = { item: cases[i][0], stmts: [] };
                                switchStmt.caseStmts.push(caseStmt);
        
                                var statements = this._collectCaseStatements(cases, i);
                                this._visitStatements(statements, caseStmt.stmts);
                                noBinding = noBinding && this._noBinding(caseStmt.stmts);
                            }
        
                            if (noBinding) {
                                return { type: "raw", stmt: ast };
                            } else {
                                return switchStmt;
                            }
                        },
        
                        "if": function (ast) {
        
                            var noBinding = true;
        
                            var ifStmt = { type: "if", conditionStmts: [] };
        
                            var currAst = ast;
                            while (true) {
                                var condition = currAst[1];
                                var condStmt = { cond: condition, stmts: [] };
                                ifStmt.conditionStmts.push(condStmt);
        
                                var thenPart = currAst[2];
                                this._visitBody(thenPart, condStmt.stmts);
        
                                noBinding = noBinding && this._noBinding(condStmt.stmts);
        
                                var elsePart = currAst[3];
                                if (elsePart && elsePart[0] == "if") {
                                    currAst = elsePart;
                                } else {
                                    break;
                                }
                            }
                
                            var elsePart = currAst[3];
                            if (elsePart) {
                                ifStmt.elseStmts = [];
        
                                this._visitBody(elsePart, ifStmt.elseStmts);
                                
                                noBinding = noBinding && this._noBinding(ifStmt.elseStmts);
                            }
        
                            if (noBinding) {
                                return { type: "raw", stmt: ast };
                            } else {
                                return ifStmt;
                            }
                        },
        
                        "try": function (ast, stmts) {
        
                            var bodyStmts = [];
                            var bodyStatements = ast[1];
                            this._visitStatements(bodyStatements, bodyStmts);
        
                            var noBinding = this._noBinding(bodyStmts)
        
                            var tryStmt = { type: "try", bodyStmt: { type: "delay", stmts: bodyStmts } };
                            
                            var catchClause = ast[2];
                            if (catchClause) {
                                var exVar = catchClause[0];
                                tryStmt.exVar = exVar;
                                tryStmt.catchStmts = [];
        
                                this._visitStatements(catchClause[1], tryStmt.catchStmts);
        
                                noBinding = noBinding && this._noBinding(tryStmt.catchStmts);
                            }
        
                            var finallyStatements = ast[3];
                            if (finallyStatements) {
                                tryStmt.finallyStmt = { type: "delay", stmts: [] };
        
                                this._visitStatements(finallyStatements, tryStmt.finallyStmt.stmts);
        
                                noBinding = noBinding && this._noBinding(tryStmt.finallyStmt.stmts);
                            }
        
                            if (noBinding) {
                                return { type: "raw", stmt: ast };
                            } else {
                                return tryStmt;
                            }
                        }
                    }
                }
        
                function CodeGenerator(builderName, binder, indent) {
                    this._builderName = builderName;
                    this._binder = binder;
                    this._normalMode = false;
                    this._indent = indent;
                    this._indentLevel = 0;
                    this._builderVar = "$$_builder_$$_" + (__jscex__tempVarSeed++);
                }
                CodeGenerator.prototype = {
                    _write: function (s) {
                        this._buffer.push(s);
                        return this;
                    },
        
                    _writeLine: function (s) {
                        this._write(s)._write("\n");
                        return this;
                    },
        
                    _writeIndents: function () {
                        for (var i = 0; i < this._indent; i++) {
                            this._write(" ");
                        }
        
                        for (var i = 0; i < this._indentLevel; i++) {
                            this._write("    ");
                        }
                        return this;
                    },
        
                    generate: function (params, jscexAst) {
                        this._buffer = [];
        
                        this._writeLine("(function (" + params.join(", ") + ") {");
                        this._indentLevel++;
        
                        this._writeIndents()
                            ._writeLine("var " + this._builderVar + " = Jscex.builders[" + stringify(this._builderName) + "];");
        
                        this._writeIndents()
                            ._writeLine("return " + this._builderVar + ".Start(this,");
                        this._indentLevel++;
        
                        this._pos = { };
        
                        this._writeIndents()
                            ._visitJscex(jscexAst)
                            ._writeLine();
                        this._indentLevel--;
        
                        this._writeIndents()
                            ._writeLine(");");
                        this._indentLevel--;
        
                        this._writeIndents()
                            ._write("})");
        
                        return this._buffer.join("");
                    },
        
                    _visitJscex: function (ast) {
                        this._jscexVisitors[ast.type].call(this, ast);
                        return this;
                    },
        
                    _visitRaw: function (ast) {
                        var type = ast[0];
        
                        function throwUnsupportedError() {
                            throw new Error('"' + type + '" is not currently supported.');
                        }
        
                        var visitor = this._rawVisitors[type];
        
                        if (visitor) {
                            visitor.call(this, ast);
                        } else {
                            throwUnsupportedError();
                        }
        
                        return this;
                    },
        
                    _visitJscexStatements: function (statements) {
                        for (var i = 0; i < statements.length; i++) {
                            var stmt = statements[i];
        
                            if (stmt.type == "raw" || stmt.type == "if" || stmt.type == "switch") {
                                this._writeIndents()
                                    ._visitJscex(stmt)._writeLine();
                            } else if (stmt.type == "delay") {
                                this._visitJscexStatements(stmt.stmts);
                            } else {
                                this._writeIndents()
                                    ._write("return ")._visitJscex(stmt)._writeLine(";");
                            }
                        }
                    },
        
                    _visitRawStatements: function (statements) {
                        for (var i = 0; i < statements.length; i++) {
                            var s = statements[i];
        
                            this._writeIndents()
                                ._visitRaw(s)._writeLine();
        
                            switch (s[0]) {
                                case "break":
                                case "return":
                                case "continue":
                                case "throw":
                                    return;
                            }
                        }
                    },
        
                    _visitRawBody: function (body) {
                        if (body[0] == "block") {
                            this._visitRaw(body);
                        } else {
                            this._writeLine();
                            this._indentLevel++;
        
                            this._writeIndents()
                                ._visitRaw(body);
                            this._indentLevel--;
                        }
        
                        return this;
                    },
        
                    _visitRawFunction: function (ast) {
                        var funcName = ast[1] || "";
                        var args = ast[2];
                        var statements = ast[3];
                        
                        this._writeLine("function " + funcName + "(" + args.join(", ") + ") {")
                        this._indentLevel++;
        
                        var currInFunction = this._pos.inFunction;
                        this._pos.inFunction = true;
        
                        this._visitRawStatements(statements);
                        this._indentLevel--;
        
                        this._pos.inFunction = currInFunction;
        
                        this._writeIndents()
                            ._write("}");
                    },
        
                    _jscexVisitors: {
                        "delay": function (ast) {
                            if (ast.stmts.length == 1) {
                                var subStmt = ast.stmts[0];
                                switch (subStmt.type) {
                                    case "delay":
                                    case "combine":
                                    case "normal":
                                    case "break":
                                    case "continue":
                                    case "loop":
                                    case "try":
                                        this._visitJscex(subStmt);
                                        return;
                                    case "return":
                                        if (!subStmt.stmt[1]) {
                                            this._visitJscex(subStmt);
                                            return;
                                        }
                                }
                            }
        
                            this._writeLine(this._builderVar + ".Delay(function () {");
                            this._indentLevel++;
        
                            this._visitJscexStatements(ast.stmts);
                            this._indentLevel--;
        
                            this._writeIndents()
                                ._write("})");
                        },
        
                        "combine": function (ast) {
                            this._writeLine(this._builderVar + ".Combine(");
                            this._indentLevel++;
        
                            this._writeIndents()
                                ._visitJscex(ast.first)._writeLine(",");
                            this._writeIndents()
                                ._visitJscex(ast.second)._writeLine();
                            this._indentLevel--;
        
                            this._writeIndents()
                                ._write(")");
                        },
        
                        "loop": function (ast) {
                            this._writeLine(this._builderVar + ".Loop(");
                            this._indentLevel++;
        
                            if (ast.condition) {
                                this._writeIndents()
                                    ._writeLine("function () {");
                                this._indentLevel++;
        
                                this._writeIndents()
                                    ._write("return ")._visitRaw(ast.condition)._writeLine(";");
                                this._indentLevel--;
        
                                this._writeIndents()
                                    ._writeLine("},");
                            } else {
                                this._writeIndents()._writeLine("null,");
                            }
        
                            if (ast.update) {
                                this._writeIndents()
                                    ._writeLine("function () {");
                                this._indentLevel++;
        
                                this._writeIndents()
                                    ._visitRaw(ast.update)._writeLine(";");
                                this._indentLevel--;
        
                                this._writeIndents()
                                    ._writeLine("},");
                            } else {
                                this._writeIndents()._writeLine("null,");
                            }
        
                            this._writeIndents()
                                ._visitJscex(ast.bodyStmt)._writeLine(",");
        
                            this._writeIndents()
                                ._writeLine(ast.bodyFirst);
                            this._indentLevel--;
        
                            this._writeIndents()
                                ._write(")");
                        },
        
                        "raw": function (ast) {
                            this._visitRaw(ast.stmt);
                        },
        
                        "bind": function (ast) {
                            var info = ast.info;
                            this._write(this._builderVar + ".Bind(")._visitRaw(info.expression)._writeLine(", function (" + info.argName + ") {");
                            this._indentLevel++;
        
                            if (info.assignee == "return") {
                                this._writeIndents()
                                    ._writeLine("return " + this._builderVar + ".Return(" + info.argName + ");");
                            } else {
                                if (info.assignee) {
                                    this._writeIndents()
                                        ._visitRaw(info.assignee)._writeLine(" = " + info.argName + ";");
                                }
        
                                this._visitJscexStatements(ast.stmts);
                            }
                            this._indentLevel--;
        
                            this._writeIndents()
                                ._write("})");
                        },
        
                        "if": function (ast) {
        
                            for (var i = 0; i < ast.conditionStmts.length; i++) {
                                var stmt = ast.conditionStmts[i];
                                
                                this._write("if (")._visitRaw(stmt.cond)._writeLine(") {");
                                this._indentLevel++;
        
                                this._visitJscexStatements(stmt.stmts);
                                this._indentLevel--;
        
                                this._writeIndents()
                                    ._write("} else ");
                            }
        
                            this._writeLine("{");
                            this._indentLevel++;
        
                            if (ast.elseStmts) {
                                this._visitJscexStatements(ast.elseStmts);
                            } else {
                                this._writeIndents()
                                    ._writeLine("return " + this._builderVar + ".Normal();");
                            }
        
                            this._indentLevel--;
        
                            this._writeIndents()
                                ._write("}");
                        },
        
                        "switch": function (ast) {
                            this._write("switch (")._visitRaw(ast.item)._writeLine(") {");
                            this._indentLevel++;
        
                            for (var i = 0; i < ast.caseStmts.length; i++) {
                                var caseStmt = ast.caseStmts[i];
        
                                if (caseStmt.item) {
                                    this._writeIndents()
                                        ._write("case ")._visitRaw(caseStmt.item)._writeLine(":");
                                } else {
                                    this._writeIndents()._writeLine("default:");
                                }
                                this._indentLevel++;
        
                                this._visitJscexStatements(caseStmt.stmts);
                                this._indentLevel--;
                            }
        
                            this._writeIndents()
                                ._write("}");
                        },
        
                        "try": function (ast) {
                            this._writeLine(this._builderVar + ".Try(");
                            this._indentLevel++;
        
                            this._writeIndents()
                                ._visitJscex(ast.bodyStmt)._writeLine(",");
        
                            if (ast.catchStmts) {
                                this._writeIndents()
                                    ._writeLine("function (" + ast.exVar + ") {");
                                this._indentLevel++;
        
                                this._visitJscexStatements(ast.catchStmts);
                                this._indentLevel--;
        
                                this._writeIndents()
                                    ._writeLine("},");
                            } else {
                                this._writeIndents()
                                    ._writeLine("null,");
                            }
        
                            if (ast.finallyStmt) {
                                this._writeIndents()
                                    ._visitJscex(ast.finallyStmt)._writeLine();
                            } else {
                                this._writeIndents()
                                    ._writeLine("null");
                            }
                            this._indentLevel--;
        
                            this._writeIndents()
                                ._write(")");
                        },
        
                        "normal": function (ast) {
                            this._write(this._builderVar + ".Normal()");
                        },
        
                        "throw": function (ast) {
                            this._write(this._builderVar + ".Throw(")._visitRaw(ast.stmt[1])._write(")");
                        },
        
                        "break": function (ast) {
                            this._write(this._builderVar + ".Break()");
                        },
        
                        "continue": function (ast) {
                            this._write(this._builderVar + ".Continue()");
                        },
        
                        "return": function (ast) {
                            this._write(this._builderVar + ".Return(");
                            if (ast.stmt[1]) this._visitRaw(ast.stmt[1]);
                            this._write(")");
                        }
                    },
        
                    _rawVisitors: {
                        "var": function (ast) {
                            this._write("var ");
        
                            var items = ast[1];
                            for (var i = 0; i < items.length; i++) {
                                this._write(items[i][0]);
                                if (items[i].length > 1) {
                                    this._write(" = ")._visitRaw(items[i][1]);
                                }
                                if (i < items.length - 1) this._write(", ");
                            }
        
                            this._write(";");
                        },
        
                        "seq": function (ast) {
                            for (var i = 1; i < ast.length; i++) {
                                this._visitRaw(ast[i]);
                                if (i < ast.length - 1) this._write(", "); 
                            }
                        },
        
                        "binary": function (ast) {
                            var op = ast[1], left = ast[2], right = ast[3];
        
                            function needBracket(item) {
                                var type = item[0];
                                return !(type == "num" || type == "name" || type == "dot");
                            }
        
                            if (needBracket(left)) {
                                this._write("(")._visitRaw(left)._write(") ");
                            } else {
                                this._visitRaw(left)._write(" ");
                            }
        
                            this._write(op);
        
                            if (needBracket(right)) {
                                this._write(" (")._visitRaw(right)._write(")");
                            } else {
                                this._write(" ")._visitRaw(right);
                            }
                        },
        
                        "sub": function (ast) {
                            var prop = ast[1], index = ast[2];
        
                            function needBracket() {
                                return !(prop[0] == "name")
                            }
        
                            if (needBracket()) {
                                this._write("(")._visitRaw(prop)._write(")[")._visitRaw(index)._write("]");
                            } else {
                                this._visitRaw(prop)._write("[")._visitRaw(index)._write("]");
                            }
                        },
        
                        "unary-postfix": function (ast) {
                            var op = ast[1];
                            var item = ast[2];
                            this._visitRaw(item)._write(op);
                        },
        
                        "unary-prefix": function (ast) {
                            var op = ast[1];
                            var item = ast[2];
                            this._write(op);
                            if (op == "typeof") {
                                this._write("(")._visitRaw(item)._write(")");
                            } else {
                                this._visitRaw(item);
                            }
                        },
        
                        "assign": function (ast) {
                            var op = ast[1];
                            var name = ast[2];
                            var value = ast[3];
        
                            this._visitRaw(name);
                            if ((typeof op) == "string") {
                                this._write(" " + op + "= ");
                            } else {
                                this._write(" = ");
                            }
                            this._visitRaw(value);
                        },
        
                        "stat": function (ast) {
                            this._visitRaw(ast[1])._write(";");
                        },
        
                        "dot": function (ast) {
                            function needBracket() {
                                var leftOp = ast[1][0];
                                return !(leftOp == "dot" || leftOp == "name");
                            }
        
                            if (needBracket()) {
                                this._write("(")._visitRaw(ast[1])._write(").")._write(ast[2]);
                            } else {
                                this._visitRaw(ast[1])._write(".")._write(ast[2]);
                            }
                        },
        
                        "new": function (ast) {
                            var ctor = ast[1];
        
                            this._write("new ")._visitRaw(ctor)._write("(");
        
                            var args = ast[2];
                            for (var i = 0, len = args.length; i < len; i++) {
                                this._visitRaw(args[i]);
                                if (i < len - 1) this._write(", ");
                            }
        
                            this._write(")");
                        },
        
                        "call": function (ast) {
                        
                            if (_isJscexPattern(ast)) {
                                var indent = this._indent + this._indentLevel * 4;
                                var newCode = _compileJscexPattern(ast, indent);
                                this._write(newCode);
                            } else {
        
                                var invalidBind = (ast[1][0] == "name") && (ast[1][1] == this._binder);
                                if (invalidBind) {
                                    this._pos = { inFunction: true };
                                    this._buffer = [];
                                }
        
                                this._visitRaw(ast[1])._write("(");
        
                                var args = ast[2];
                                for (var i = 0; i < args.length; i++) {
                                    this._visitRaw(args[i]);
                                    if (i < args.length - 1) this._write(", ");
                                }
        
                                this._write(")");
        
                                if (invalidBind) {
                                    throw ("Invalid bind operation: " + this._buffer.join(""));
                                }
                            }
                        },
        
                        "name": function (ast) {
                            this._write(ast[1]);
                        },
        
                        "object": function (ast) {
                            var items = ast[1];
                            if (items.length <= 0) {
                                this._write("{ }");
                            } else {
                                this._writeLine("{");
                                this._indentLevel++;
                                
                                for (var i = 0; i < items.length; i++) {
                                    this._writeIndents()
                                        ._write(stringify(items[i][0]) + ": ")
                                        ._visitRaw(items[i][1]);
                                    
                                    if (i < items.length - 1) {
                                        this._writeLine(",");
                                    } else {
                                        this._writeLine("");
                                    }
                                }
                                
                                this._indentLevel--;
                                this._writeIndents()._write("}");
                            }
                        },
        
                        "array": function (ast) {
                            this._write("[");
        
                            var items = ast[1];
                            for (var i = 0; i < items.length; i++) {
                                this._visitRaw(items[i]);
                                if (i < items.length - 1) this._write(", ");
                            }
        
                            this._write("]");
                        },
        
                        "num": function (ast) {
                            this._write(ast[1]);
                        },
        
                        "regexp": function (ast) {
                            this._write("/" + ast[1] + "/" + ast[2]);
                        },
        
                        "string": function (ast) {
                            this._write(stringify(ast[1]));
                        },
        
                        "function": function (ast) {
                            this._visitRawFunction(ast);
                        },
        
                        "defun": function (ast) {
                            this._visitRawFunction(ast);
                        },
        
                        "return": function (ast) {
                            if (this._pos.inFunction) {
                                this._write("return");
                                var value = ast[1];
                                if (value) this._write(" ")._visitRaw(value);
                                this._write(";");
                            } else {
                                this._write("return ")._visitJscex({ type: "return", stmt: ast })._write(";");
                            }
                        },
                        
                        "for": function (ast) {
                            this._write("for (");
        
                            var setup = ast[1];
                            if (setup) {
                                this._visitRaw(setup);
                                if (setup[0] != "var") {
                                    this._write("; ");
                                } else {
                                    this._write(" ");
                                }
                            } else {
                                this._write("; ");
                            }
        
                            var condition = ast[2];
                            if (condition) this._visitRaw(condition);
                            this._write("; ");
        
                            var update = ast[3];
                            if (update) this._visitRaw(update);
                            this._write(") ");
        
                            var currInLoop = this._pos.inLoop;
                            this._pos.inLoop = true;
        
                            var body = ast[4];
                            this._visitRawBody(body);
        
                            this._pos.inLoop = currInLoop;
                        },
        
                        "for-in": function (ast) {
                            this._write("for (");
        
                            var declare = ast[1];
                            if (declare[0] == "var") { // declare == ["var", [["m"]]]
                                this._write("var " + declare[1][0][0]);
                            } else {
                                this._visitRaw(declare);
                            }
                            
                            this._write(" in ")._visitRaw(ast[3])._write(") ");
        
                            var body = ast[4];
                            this._visitRawBody(body);
                        },
        
                        "block": function (ast) {
                            this._writeLine("{")
                            this._indentLevel++;
        
                            this._visitRawStatements(ast[1]);
                            this._indentLevel--;
        
                            this._writeIndents()
                                ._write("}");
                        },
        
                        "while": function (ast) {
                            var condition = ast[1];
                            var body = ast[2];
        
                            var currInLoop = this._pos.inLoop
                            this._pos.inLoop = true;
        
                            this._write("while (")._visitRaw(condition)._write(") ")._visitRawBody(body);
        
                            this._pos.inLoop = currInLoop;
                        },
        
                        "do": function (ast) {
                            var condition = ast[1];
                            var body = ast[2];
        
                            var currInLoop = this._pos.inLoop;
                            this._pos.inLoop = true;
        
                            this._write("do ")._visitRawBody(body);
        
                            this._pos.inLoop = currInLoop;
        
                            if (body[0] == "block") {
                                this._write(" ");
                            } else {
                                this._writeLine()._writeIndents();
                            }
        
                            this._write("while (")._visitRaw(condition)._write(");");
                        },
        
                        "if": function (ast) {
                            var condition = ast[1];
                            var thenPart = ast[2];
        
                            this._write("if (")._visitRaw(condition)._write(") ")._visitRawBody(thenPart);
        
                            var elsePart = ast[3];
                            if (elsePart) {
                                if (thenPart[0] == "block") {
                                    this._write(" ");
                                } else {
                                    this._writeLine("")
                                        ._writeIndents();
                                }
        
                                if (elsePart[0] == "if") {
                                    this._write("else ")._visitRaw(elsePart);
                                } else {
                                    this._write("else ")._visitRawBody(elsePart);
                                }
                            }
                        },
        
                        "break": function (ast) {
                            if (this._pos.inLoop || this._pos.inSwitch) {
                                this._write("break;");
                            } else {
                                this._write("return ")._visitJscex({ type: "break", stmt: ast })._write(";");
                            }
                        },
        
                        "continue": function (ast) {
                            if (this._pos.inLoop) {
                                this._write("continue;");
                            } else {
                                this._write("return ")._visitJscex({ type: "continue", stmt: ast })._write(";");
                            }
                        },
        
                        "throw": function (ast) {
                            var pos = this._pos;
                            if (pos.inTry || pos.inFunction) {
                                this._write("throw ")._visitRaw(ast[1])._write(";");
                            } else {
                                this._write("return ")._visitJscex({ type: "throw", stmt: ast })._write(";");
                            }
                        },
        
                        "conditional": function (ast) {
                            this._write("(")._visitRaw(ast[1])._write(") ? (")._visitRaw(ast[2])._write(") : (")._visitRaw(ast[3])._write(")");
                        },
        
                        "try": function (ast) {
        
                            this._writeLine("try {");
                            this._indentLevel++;
        
                            var currInTry = this._pos.inTry;
                            this._pos.inTry = true;
        
                            this._visitRawStatements(ast[1]);
                            this._indentLevel--;
        
                            this._pos.inTry = currInTry;
        
                            var catchClause = ast[2];
                            var finallyStatements = ast[3];
        
                            if (catchClause) {
                                this._writeIndents()
                                    ._writeLine("} catch (" + catchClause[0] + ") {")
                                this._indentLevel++;
        
                                this._visitRawStatements(catchClause[1]);
                                this._indentLevel--;
                            }
        
                            if (finallyStatements) {
                                this._writeIndents()
                                    ._writeLine("} finally {");
                                this._indentLevel++;
        
                                this._visitRawStatements(finallyStatements);
                                this._indentLevel--;
                            }                
        
                            this._writeIndents()
                                ._write("}");
                        },
        
                        "switch": function (ast) {
                            this._write("switch (")._visitRaw(ast[1])._writeLine(") {");
                            this._indentLevel++;
        
                            var currInSwitch = this._pos.inSwitch;
                            this._pos.inSwitch = true;
        
                            var cases = ast[2];
                            for (var i = 0; i < cases.length; i++) {
                                var c = cases[i];
                                this._writeIndents();
        
                                if (c[0]) {
                                    this._write("case ")._visitRaw(c[0])._writeLine(":");
                                } else {
                                    this._writeLine("default:");
                                }
                                this._indentLevel++;
        
                                this._visitRawStatements(c[1]);
                                this._indentLevel--;
                            }
                            this._indentLevel--;
        
                            this._pos.inSwitch = currInSwitch;
        
                            this._writeIndents()
                                ._write("}");
                        }
                    }
                }
        
                function _isJscexPattern(ast) {
                    if (ast[0] != "call") return false;
                    
                    var evalName = ast[1];
                    if (evalName[0] != "name" || evalName[1] != "eval") return false;
        
                    var compileCall = ast[2][0];
                    if (!compileCall || compileCall[0] != "call") return false;
        
                    var compileMethod = compileCall[1];
                    if (!compileMethod || compileMethod[0] != "dot" || compileMethod[2] != "compile") return false;
        
                    var jscexName = compileMethod[1];
                    if (!jscexName || jscexName[0] != "name" || jscexName[1] != "Jscex") return false;
        
                    var builder = compileCall[2][0];
                    if (!builder || builder[0] != "string") return false;
        
                    var func = compileCall[2][1];
                    if (!func || func[0] != "function") return false;
        
                    return true;
                }
                
                function _compileJscexPattern(ast, indent) {
        
                    var builderName = ast[2][0][2][0][1];
                    var funcAst = ast[2][0][2][1];
                    var binder = root.binders[builderName];
        
                    var jscexTreeGenerator = new JscexTreeGenerator(binder);
                    var jscexAst = jscexTreeGenerator.generate(funcAst);
        
                    var codeGenerator = new CodeGenerator(builderName, binder, indent);
                    var newCode = codeGenerator.generate(funcAst[2], jscexAst);
        
                    return newCode;
                }
                
                function compile(builderName, func) {
        
                    var funcCode = func.toString();
                    var evalCode = "eval(Jscex.compile(" + stringify(builderName) + ", " + funcCode + "))"
                    var evalCodeAst = root.parse(evalCode);
        
                    // [ "toplevel", [ [ "stat", [ "call", ... ] ] ] ]
                    var evalAst = evalCodeAst[1][0][1];
                    var newCode = _compileJscexPattern(evalAst, 0);
        
                    root.logger.debug(funcCode + "\n\n>>>\n\n" + newCode);
                    
                    return codeGenerator(newCode);
                };
        
                root.compile = compile;
                
                root.modules["jit"] = true;
            }
            
            var isCommonJS = (typeof require !== "undefined" && typeof module !== "undefined" && module.exports);
            var isAmd = (typeof define !== "undefined" && define.amd);
            
            if (isCommonJS) {
                module.exports.init = function (root) {
                    if (!root.modules["parser"]) {
                        require("./jscex-parser").init(root);
                    };
                    
                    init(root);
                }
            } else if (isAmd) {
                define("jscex-jit", ["jscex-parser"], function (parser) {
                    return {
                        init: function (root) {
                            if (!root.modules["parser"]) {
                                parser.init(root);
                            }
                            
                            init(root);
                        }
                    };
                });
            } else {
                if (typeof Jscex === "undefined") {
                    throw new Error('Missing root object, please load "jscex" module first.');
                }
                
                if (!Jscex.modules["parser"]) {
                    throw new Error('Missing essential components, please initialize "parser" module first.');
                }
        
                init(Jscex);
            }
        
        })();
        </script>
		<script> (function(){var j=function(){};j.prototype={Loop:function(b,c,a,d){return{next:function(e,i){var f=function(b){a.next(e,function(a,e){if(a=="normal"||a=="continue")g(b);else if(a=="throw"||a=="return")i(a,e);else if(a=="break")i("normal");else throw Error('Invalid type for "Loop": '+a);})},g=function(a){try{c&&!a&&c.call(e),!b||b.call(e)?f(!1):i("normal")}catch(d){i("throw",d)}};d?f(!0):g(!0)}}},Delay:function(b){return{next:function(c,a){try{b.call(c).next(c,a)}catch(d){a("throw",d)}}}},Combine:function(b,
            c){return{next:function(a,d){b.next(a,function(b,i,f){if(b=="normal")try{c.next(a,d)}catch(g){d("throw",g)}else d(b,i,f)})}}},Return:function(b){return{next:function(c,a){a("return",b)}}},Normal:function(){return{next:function(b,c){c("normal")}}},Break:function(){return{next:function(b,c){c("break")}}},Continue:function(){return{next:function(b,c){c("continue")}}},Throw:function(b){return{next:function(c,a){a("throw",b)}}},Try:function(b,c,a){return{next:function(d,e){b.next(d,function(b,f,g){if(b!=
            "throw"||!c)a?a.next(d,function(a,c,d){a=="normal"?e(b,f,g):e(a,c,d)}):e(b,f,g);else if(c){var h;try{h=c.call(d,f)}catch(j){a?a.next(d,function(a,b,c){a=="normal"?e("throw",j):e(a,b,c)}):e("throw",j)}h&&h.next(d,function(b,c,f){b=="throw"?a?a.next(d,function(a,d,g){a=="normal"?e(b,c,f):e(a,d,g)}):e(b,c,f):a?a.next(d,function(a,d,g){a=="normal"?e(b,c,f):e(a,d,g)}):e(b,c,f)})}else a.next(d,function(a,c,d){a=="normal"?e(b,f,g):e(a,c,d)})})}}}};var h=function(b){if(!b.modules)b.modules={};if(!b.modules.builderbase)b.modules.builderbase=
            !0,b.BuilderBase=j},k=typeof define==="function"&&!define.amd,l=typeof require==="function"&&typeof define==="function"&&define.amd;if(typeof require==="function"&&typeof module!=="undefined"&&module.exports)module.exports.init=h;else if(k)define("jscex-builderbase",function(b,c,a){a.exports.init=h});else if(l)define("jscex-builderbase",function(){return{init:h}});else{if(typeof Jscex==="undefined")throw Error('Missing the root object, please load "jscex" module first.');h(Jscex)}})();
            </script>
		<script> (function(){var k=function(){};k.prototype={isCancellation:!0,message:"The task has been cancelled."};typeof __jscex__async__taskIdSeed==="undefined"&&(__jscex__async__taskIdSeed=0);var l=function(b){return typeof b.start==="function"&&typeof b.addEventListener==="function"&&typeof b.removeEventListener==="function"&&typeof b.complete==="function"},j=function(b){if(!b.modules.async){var d=function(){};d.prototype={register:function(a){this.isCancellationRequested&&a();if(!this._handlers)this._handlers=
            [];this._handlers.push(a)},unregister:function(a){this._handlers&&(a=this._handlers.indexOf(a),a>=0&&this._handlers.splice(a,1))},cancel:function(){if(!this.isCancellationRequested){this.isCancellationRequested=!0;var a=this._handlers;delete this._handlers;for(var f=0;f<a.length;f++)try{a[f]()}catch(c){b.logger.warn("[WARNING] Cancellation handler threw an error: "+c)}}},throwIfCancellationRequested:function(){if(this.isCancellationRequested)throw new k;}};var e=function(a){this.id=++__jscex__async__taskIdSeed;
            this._delegate=a;this._listeners={};this.status="ready"};e.prototype={start:function(){if(this.status!="ready")throw Error('Task can only be started in "ready" status.');this.status="running";this._delegate(this)},complete:function(a,f){if(this.status!="running")throw Error('The "complete" method can only be called in "running" status.');var c=this._listeners;delete this._listeners;if(a=="success")this.result=f,this.status="succeeded",this._notify("success",c.success);else if(a=="failure")this.error=
            f,this.status=f.isCancellation?"canceled":"faulted",this._notify("failure",c.failure);else throw Error("Unsupported type: "+a);this._notify("complete",c.complete);this.error&&!c.failure&&!c.complete&&b.logger.warn("[WARNING] An unhandled error occurred: "+this.error)},_notify:function(a,f){if(f)for(var c=0;c<f.length;c++)try{f[c](this)}catch(i){b.logger.warn("[WARNING] The task's "+a+" listener threw an error: "+i)}},addEventListener:function(a,b){this._listeners&&(this._listeners[a]||(this._listeners[a]=
            []),this._listeners[a].push(b))},removeEventListener:function(a,b){if(this._listeners){var c=this._listeners[a];if(c){var i=c.indexOf(b);i>=0&&c.splice(i,1)}}}};e.create=function(a){return new e(a)};e.isTask=l;var h=function(){};h.prototype={Start:function(a,b){return e.create(function(c){b.next(a,function(a,b){if(a=="normal"||a=="return")c.complete("success",b);else if(a=="throw")c.complete("failure",b);else throw Error("Unsupported type: "+a);})})},Bind:function(a,b){return{next:function(c,e){var d=
            function(a){if(a.error)e("throw",a.error);else{var d;try{d=b.call(c,a.result)}catch(h){e("throw",h);return}d.next(c,e)}};a.status=="ready"?(a.addEventListener("complete",d),a.start()):a.status=="running"?a.addEventListener("complete",d):d(a)}}}};for(var g in b.BuilderBase.prototype)h.prototype[g]=b.BuilderBase.prototype[g];if(!b.Async)b.Async={};g=b.Async;g.CancellationToken=d;g.CanceledError=k;g.Task=e;g.AsyncBuilder=h;if(!b.builders)b.builders={};b.binders.async="$await";b.builders.async=new h;
            b.modules.async=!0}},m=typeof define==="function"&&!define.amd,n=typeof require==="function"&&typeof define==="function"&&define.amd;if(typeof require==="function"&&typeof module!=="undefined"&&module.exports)module.exports.init=function(b){if(!b.modules.builderbase){if(typeof __dirname==="string")try{require.paths.unshift(__dirname)}catch(d){try{module.paths.unshift(__dirname)}catch(e){}}require("jscex-builderbase").init(b)}j(b)};else if(m)define("jscex-async",["jscex-builderbase"],function(b,d,
            e){e.exports.init=function(d){d.modules.builderbase||b("jscex-builderbase").init(d);j(d)}});else if(n)define("jscex-async",["jscex-builderbase"],function(b){return{init:function(d){d.modules.builderbase||b.init(d);j(d)}}});else{if(typeof Jscex==="undefined")throw Error('Missing the root object, please load "jscex" module first.');if(!Jscex.modules.builderbase)throw Error('Missing essential components, please initialize "builderbase" module first.');j(Jscex)}})();
            </script>
		<script> (function(){var m=function(j){if(j.length<=1)return null;for(var f=[],h=1;h<j.length;h++)f.push(j[h]);return f},n=function(j,f){for(var h=[],k=0;k<j.length;k++)h.push(j[k]);for(;h.length<f;)h.push(void 0);return h},l=function(j){if(!j.modules["async-powerpack"]){if(!j.modules.async)throw Error('Missing essential components, please initialize "jscex-async" module first.');var f=j.Async,h=f.Task,k=f.CanceledError;f.sleep=function(a,b){return h.create(function(c){b&&b.isCancellationRequested&&c.complete("failure",
            new k);var e,d;b&&(d=function(){clearTimeout(e);c.complete("failure",new k)});e=setTimeout(function(){b&&b.unregister(d);c.complete("success")},a);b&&b.register(d)})};f.onEvent=function(a,b,c){return h.create(function(e){c&&c.isCancellationRequested&&e.complete("failure",new k);var d=function(){a.removeEventListener?a.removeEventListener(b,g):a.removeListener?a.removeListener(b,g):a.detachEvent(b,g)},g,i;c&&(i=function(){d();e.complete("failure",new k)});g=function(a){c&&c.unregister(i);d();e.complete("success",
            a)};a.addEventListener?a.addEventListener(b,g):a.addListener?a.addListener(b,g):a.attachEvent(b,g);c&&c.register(i)})};h.whenAll=function(){var a={},b;if(arguments.length==1){var c=arguments[0];h.isTask(c)?(a[0]=c,b=!0):(a=c,b=Object.prototype.toString.call(a)==="[object Array]")}else{for(c=0;c<arguments.length;c++)a[c]=arguments[c];b=!0}return h.create(function(e){var d={},g;for(g in a)if(a.hasOwnProperty(g)){var i=a[g];h.isTask(i)&&(d[i.id]=g)}for(var c in d)i=a[d[c]],i.status=="ready"&&i.start();
            for(c in d)if(i=a[d[c]],i.error){e.complete("failure",i.error);return}var f=b?[]:{},j=function(b){if(b.error){for(var c in d)a[d[c]].removeEventListener("complete",j);e.complete("failure",b.error)}else f[d[b.id]]=b.result,delete d[b.id],k--,k==0&&e.complete("success",f)},k=0;for(c in d)g=d[c],i=a[g],i.status=="succeeded"?(f[g]=i.result,delete d[i.id]):(k++,i.addEventListener("complete",j));k==0&&e.complete("success",f)})};h.whenAny=function(){var a={};if(arguments.length==1){var b=arguments[0];h.isTask(b)?
            a[0]=b:a=b}else for(b=0;b<arguments.length;b++)a[b]=arguments[b];return h.create(function(b){var e={},d;for(d in a)if(a.hasOwnProperty(d)){var g=a[d];h.isTask(g)&&(e[g.id]=d)}for(var i in e)g=a[e[i]],g.status=="ready"&&g.start();for(i in e)if(d=e[i],g=a[d],g.error||g.status=="succeeded"){b.complete("success",{key:d,task:g});return}var f=function(d){for(var g in e)a[e[g]].removeEventListener("complete",f);b.complete("success",{key:e[d.id],task:d})};for(i in e)a[e[i]].addEventListener("complete",f)})};
            if(!f.Jscexify)f.Jscexify={};f=f.Jscexify;f.fromStandard=function(a){var b=m(arguments);return function(){var c=this,e=n(arguments,a.length-1);return h.create(function(d){e.push(function(a,c){if(a)d.complete("failure",a);else if(b){for(var e={},f=0;f<b.length;f++)e[b[f]]=arguments[f+1];return d.complete("success",e)}else d.complete("success",c)});a.apply(c,e)})}};f.fromCallback=function(a){var b=m(arguments);return function(){var c=this,e=n(arguments,a.length-1);return h.create(function(d){e.push(function(a){if(b){for(var c=
            {},e=0;e<b.length;e++)c[b[e]]=arguments[e];d.complete("success",c)}else d.complete("success",a)});a.apply(c,e)})}};j.modules["async-powerpack"]=!0}},o=typeof define==="function"&&!define.amd,p=typeof require==="function"&&typeof define==="function"&&define.amd;if(typeof require==="function"&&typeof module!=="undefined"&&module.exports)module.exports.init=l;else if(o)define("jscex-async-powerpack",["jscex-async"],function(j,f,h){h.exports.init=l});else if(p)define("jscex-async-powerpack",["jscex-async"],
            function(){return{init:l}});else{if(typeof Jscex==="undefined")throw Error('Missing the root object, please load "jscex" module first.');l(Jscex)}})();
            </script>
		<script> 

            // variables
            var $win = $(window);
            var clientWidth = $win.width();
            var clientHeight = $win.height();
            
            $(window).resize(function() {
                var newWidth = $win.width();
                var newHeight = $win.height();
                if (newWidth != clientWidth && newHeight != clientHeight) {
                    location.replace(location);
                }
            });
            
            (function($) {
                $.fn.typewriter = function() {
                    this.each(function() {
                        var $ele = $(this), str = $ele.html(), progress = 0;
                        $ele.html('');
                        var timer = setInterval(function() {
                            var current = str.substr(progress, 1);
                            if (current == '<') {
                                progress = str.indexOf('>', progress) + 1;
                            } else {
                                progress++;
                            }
                            $ele.html(str.substring(0, progress) + (progress & 1 ? '_' : ''));
                            if (progress >= str.length) {
                                clearInterval(timer);
                            }
                        }, 75);
                    });
                    return this;
                };
            })(jQuery);
            
            function timeElapse(date){
                var current = Date();
                var seconds = (Date.parse(current) - Date.parse(date)) / 1000;
                var days = Math.floor(seconds / (3600 * 24));
                seconds = seconds % (3600 * 24);
                var hours = Math.floor(seconds / 3600);
                if (hours < 10) {
                    hours = "0" + hours;
                }
                seconds = seconds % 3600;
                var minutes = Math.floor(seconds / 60);
                if (minutes < 10) {
                    minutes = "0" + minutes;
                }
                seconds = seconds % 60;
                if (seconds < 10) {
                    seconds = "0" + seconds;
                }
                var result = "Days <span class=\"digit\">" + days + "</span> Hours <span class=\"digit\">" + hours + "</span> Minutes <span class=\"digit\">" + minutes; 
                $("#clock").html(result);
            
                var text = "THE WORLD JUST GOT LUCKIER SINCE ";
                $("#message-box").html(text);
            
            }
            </script>
		<script> (function(window){

            function random(min, max) {
                return min + Math.floor(Math.random() * (max - min + 1));
            }
        
            function bezier(cp, t) {  
                var p1 = cp[0].mul((1 - t) * (1 - t));
                var p2 = cp[1].mul(2 * t * (1 - t));
                var p3 = cp[2].mul(t * t); 
                return p1.add(p2).add(p3);
            }  
        
            function inheart(x, y, r) {
                
                var z = ((x / r) * (x / r) + (y / r) * (y / r) - 1) * ((x / r) * (x / r) + (y / r) * (y / r) - 1) * ((x / r) * (x / r) + (y / r) * (y / r) - 1) - (x / r) * (x / r) * (y / r) * (y / r) * (y / r);
                return z < 0;
            }
        
            Point = function(x, y) {
                this.x = x || 0;
                this.y = y || 0;
            }
            Point.prototype = {
                clone: function() {
                    return new Point(this.x, this.y);
                },
                add: function(o) {
                    p = this.clone();
                    p.x += o.x;
                    p.y += o.y;
                    return p;
                },
                sub: function(o) {
                    p = this.clone();
                    p.x -= o.x;
                    p.y -= o.y;
                    return p;
                },
                div: function(n) {
                    p = this.clone();
                    p.x /= n;
                    p.y /= n;
                    return p;
                },
                mul: function(n) {
                    p = this.clone();
                    p.x *= n;
                    p.y *= n;
                    return p;
                }
            }
        
            Heart = function() {
                // x = 16 sin^3 t
                // y = 13 cos t - 5 cos 2t - 2 cos 3t - cos 4t
                // http://www.wolframalpha.com/input/?i=x+%3D+16+sin%5E3+t%2C+y+%3D+(13+cos+t+-+5+cos+2t+-+2+cos+3t+-+cos+4t)
                var points = [], x, y, t;
                for (var i = 10; i < 30; i += 0.2) {
                    t = i / Math.PI;
                    x = 16 * Math.pow(Math.sin(t), 3);
                    y = 13 * Math.cos(t) - 5 * Math.cos(2 * t) - 2 * Math.cos(3 * t) - Math.cos(4 * t);
                    points.push(new Point(x, y));
                }
                this.points = points;
                this.length = points.length;
            }
            Heart.prototype = {
                get: function(i, scale) {
                    return this.points[i].mul(scale || 1);
                }
            }
        
            Seed = function(tree, point, scale, color) {
                this.tree = tree;
        
                var scale = scale || 1
                var color = '#FFC0CB';
        
                this.heart = {
                    point  : point,
                    scale  : scale,
                    color  : color,
                    figure : new Heart(),
                }
        
                this.cirle = {
                    point  : point,
                    scale  : scale,
                    color  : color,
                    radius : 5,
                }
            }
            Seed.prototype = {
                draw: function() {
                    this.drawHeart();
                    this.drawText();
                },
                addPosition: function(x, y) {
                    this.cirle.point = this.cirle.point.add(new Point(x, y));
                },
                canMove: function() {
                    return this.cirle.point.y < (this.tree.height + 20); 
                },
                move: function(x, y) {
                    this.clear();
                    this.drawCirle();
                    this.addPosition(x, y);
                },
                canScale: function() {
                    return this.heart.scale > 0.2;
                },
                setHeartScale: function(scale) {
                    this.heart.scale *= scale;
                },
                scale: function(scale) {
                    this.clear();
                    this.drawCirle();
                    this.drawHeart();
                    this.setHeartScale(scale);
                },
                drawHeart: function() {
                    var ctx = this.tree.ctx, heart = this.heart;
                    var point = heart.point, color = heart.color, 
                        scale = heart.scale;
                    ctx.save();
                    ctx.fillStyle = color;
                    ctx.translate(point.x, point.y);
                    ctx.beginPath();
                    ctx.moveTo(0, 0);
                    for (var i = 0; i < heart.figure.length; i++) {
                        var p = heart.figure.get(i, scale);
                        ctx.lineTo(p.x, -p.y);
                    }
                    ctx.closePath();
                    ctx.fill();
                    ctx.restore();
                },
                drawCirle: function() {
                    var ctx = this.tree.ctx, cirle = this.cirle;
                    var point = cirle.point, color = cirle.color, 
                        scale = cirle.scale, radius = cirle.radius;
                    ctx.save();
                    ctx.fillStyle = color;
                    ctx.translate(point.x, point.y);
                    ctx.scale(scale, scale);
                    ctx.beginPath();
                    ctx.moveTo(0, 0);
                    ctx.arc(0, 0, radius, 0, 2 * Math.PI);
                    ctx.closePath();
                    ctx.fill();
                    ctx.restore();
                },
                drawText: function() {
                    var ctx = this.tree.ctx, heart = this.heart;
                    var point = heart.point, color = heart.color, 
                        scale = heart.scale;
                    ctx.save();
                    ctx.strokeStyle = color;
                    ctx.fillStyle = color;
                    ctx.translate(point.x, point.y);
                    ctx.scale(scale, scale);
                    ctx.moveTo(0, 0);
                    ctx.lineTo(15, 15);
                    ctx.lineTo(130, 15);
                    ctx.stroke();
        
                    ctx.moveTo(0, 0);
                    ctx.scale(0.75, 0.75);
                    ctx.font = "12px,Verdana"; // 字号肿么没有用? (ˉ(∞)ˉ)
                    ctx.fillText("Click Me:) ", 30, -5);
                    ctx.fillText("Birthday Queen !", 28, 10);
                    ctx.restore();
                },
                clear: function() {
                    var ctx = this.tree.ctx, cirle = this.cirle;
                    var point = cirle.point, scale = cirle.scale, radius = 26;
                    var w = h = (radius * scale);
                    ctx.clearRect(point.x - w, point.y - h, 4 * w, 4 * h);
                },
                hover: function(x, y) {
                    var ctx = this.tree.ctx;
                    var pixel = ctx.getImageData(x, y, 1, 1);
                    return pixel.data[3] == 255
                }
            }
        
            Footer = function(tree, width, height, speed) {
                this.tree = tree;
                this.point = new Point(tree.seed.heart.point.x, tree.height - height / 2);
                this.width = width;
                this.height = height;
                this.speed = speed || 2;
                this.length = 0;
            }
            Footer.prototype = {
                draw: function() {
                    var ctx = this.tree.ctx, point = this.point;
                    var len = this.length / 2;
        
                    ctx.save();
                    ctx.strokeStyle = '#FFF';
                    ctx.lineWidth = this.height;
                    ctx.lineCap = 'round';
                    ctx.lineJoin = 'round';
                    ctx.translate(point.x, point.y);
                    ctx.beginPath();
                    ctx.moveTo(0, 0);
                    ctx.lineTo(len, 0);
                    ctx.lineTo(-len, 0);
                    ctx.stroke();
                    ctx.restore();
        
                    if (this.length < this.width) {
                        this.length += this.speed;
                    }
                }
            }
        
            Tree = function(canvas, width, height, opt) {
                this.canvas = canvas;
                this.ctx = canvas.getContext('2d');
                this.width = width;
                this.height = height;
                this.opt = opt || {};
        
                this.record = {};
                
                this.initSeed();
                this.initFooter();
                this.initBranch();
                this.initBloom();
            }
            Tree.prototype = {
                initSeed: function() {
                    var seed = this.opt.seed || {};
                    var x = seed.x || this.width / 2;
                    var y = seed.y || this.height / 2;
                    var point = new Point(x, y);
                    var color = seed.color || '#FF0000';
                    var scale = seed.scale || 1;
        
                    this.seed = new Seed(this, point, scale, color);
                },
        
                initFooter: function() {
                    var footer = this.opt.footer || {};
                    var width = footer.width || this.width;
                    var height = footer.height || 5;
                    var speed = footer.speed || 2;
                    this.footer = new Footer(this, width, height, speed);
                },
        
                initBranch: function() {
                    var branchs = this.opt.branch || []
                    this.branchs = [];
                    this.addBranchs(branchs);
                },
        
                initBloom: function() {
                    var bloom = this.opt.bloom || {};
                    var cache = [],
                        num = bloom.num || 500, 
                        width = bloom.width || this.width,
                        height = bloom.height || this.height,
                        figure = this.seed.heart.figure;
                    var r = 240, x, y;
                    for (var i = 0; i < num; i++) {
                        cache.push(this.createBloom(width, height, r, figure));
                    }
                    this.blooms = [];
                    this.bloomsCache = cache;
                },
        
                toDataURL: function(type) {
                    return this.canvas.toDataURL(type);
                },
        
                draw: function(k) {
                    var s = this, ctx = s.ctx;
                    var rec = s.record[k];
                    if (!rec) {
                        return ;
                    }
                    var point = rec.point,
                        image = rec.image;
        
                    ctx.save();
                    ctx.putImageData(image, point.x, point.y);
                    ctx.restore();
                },
        
                addBranch: function(branch) {
                    this.branchs.push(branch);
                },
        
                addBranchs: function(branchs){
                    var s = this, b, p1, p2, p3, r, l, c;
                    for (var i = 0; i < branchs.length; i++) {
                        b = branchs[i];
                        p1 = new Point(b[0], b[1]);
                        p2 = new Point(b[2], b[3]);
                        p3 = new Point(b[4], b[5]);
                        r = b[6];
                        l = b[7];
                        c = b[8]
                        s.addBranch(new Branch(s, p1, p2, p3, r, l, c)); 
                    }
                },
        
                removeBranch: function(branch) {
                    var branchs = this.branchs;
                    for (var i = 0; i < branchs.length; i++) {
                        if (branchs[i] === branch) {
                            branchs.splice(i, 1);
                        }
                    }
                },
        
                canGrow: function() {
                    return !!this.branchs.length;
                },
                grow: function() {
                    var branchs = this.branchs;
                    for (var i = 0; i < branchs.length; i++) {
                        var branch = branchs[i];
                        if (branch) {
                            branch.grow();
                        }
                    }
                },
        
                addBloom: function (bloom) {
                    this.blooms.push(bloom);
                },
        
                removeBloom: function (bloom) {
                    var blooms = this.blooms;
                    for (var i = 0; i < blooms.length; i++) {
                        if (blooms[i] === bloom) {
                            blooms.splice(i, 1);
                        }
                    }
                },
        
                createBloom: function(width, height, radius, figure, color, alpha, angle, scale, place, speed) {
                    var x, y;
                    while (true) {
                        x = random(20, width - 20);
                        y = random(20, height - 20);
                        if (inheart(x - width / 2, height - (height - 40) / 2 - y, radius)) {
                            return new Bloom(this, new Point(x, y), figure, color, alpha, angle, scale, place, speed);
                        }
                    }
                },
                
                canFlower: function() {
                    return !!this.blooms.length;
                }, 
                flower: function(num) {
                    var s = this, blooms = s.bloomsCache.splice(0, num);
                    for (var i = 0; i < blooms.length; i++) {
                        s.addBloom(blooms[i]);
                    }
                    blooms = s.blooms;
                    for (var j = 0; j < blooms.length; j++) {
                        blooms[j].flower();
                    }
                },
        
                snapshot: function(k, x, y, width, height) {
                    var ctx = this.ctx;
                    var image = ctx.getImageData(x, y, width, height); 
                    this.record[k] = {
                        image: image,
                        point: new Point(x, y),
                        width: width,
                        height: height
                    }
                },
                setSpeed: function(k, speed) {
                    this.record[k || "move"].speed = speed;
                },
                move: function(k, x, y) {
                    var s = this, ctx = s.ctx;
                    var rec = s.record[k || "move"];
                    var point = rec.point,
                        image = rec.image,
                        speed = rec.speed || 10,
                        width = rec.width,
                        height = rec.height; 
        
                    i = point.x + speed < x ? point.x + speed : x;
                    j = point.y + speed < y ? point.y + speed : y; 
        
                    ctx.save();
                    ctx.clearRect(point.x, point.y, width, height);
                    ctx.putImageData(image, i, j);
                    ctx.restore();
        
                    rec.point = new Point(i, j);
                    rec.speed = speed * 0.95;
        
                    if (rec.speed < 2) {
                        rec.speed = 2;
                    }
                    return i < x || j < y;
                },
        
                jump: function() {
                    var s = this, blooms = s.blooms;
                    if (blooms.length) {
                        for (var i = 0; i < blooms.length; i++) {
                            blooms[i].jump();
                        }
                    } 
                    if ((blooms.length && blooms.length < 3) || !blooms.length) {
                        var bloom = this.opt.bloom || {},
                            width = bloom.width || this.width,
                            height = bloom.height || this.height,
                            figure = this.seed.heart.figure;
                        var r = 240, x, y;
                        for (var i = 0; i < random(1,2); i++) {
                            blooms.push(this.createBloom(width / 2 + width, height, r, figure, null, 1, null, 1, new Point(random(-100,600), 720), random(200,300)));
                        }
                    }
                }
            }
        
            Branch = function(tree, point1, point2, point3, radius, length, branchs) {
                this.tree = tree;
                this.point1 = point1;
                this.point2 = point2;
                this.point3 = point3;
                this.radius = radius;
                this.length = length || 100;    
                this.len = 0;
                this.t = 1 / (this.length - 1);   
                this.branchs = branchs || [];
            }
        
            Branch.prototype = {
                grow: function() {
                    var s = this, p; 
                    if (s.len <= s.length) {
                        p = bezier([s.point1, s.point2, s.point3], s.len * s.t);
                        s.draw(p);
                        s.len += 1;
                        s.radius *= 0.97;
                    } else {
                        s.tree.removeBranch(s);
                        s.tree.addBranchs(s.branchs);
                    }
                },
                draw: function(p) {
                    var s = this;
                    var ctx = s.tree.ctx;
                    ctx.save();
                    ctx.beginPath();
                    ctx.fillStyle = '#FFC0CB';
                    // ctx.shadowColor = 'rgb(35, 31, 32)';
                    ctx.shadowBlur = 2;
                    ctx.moveTo(p.x, p.y);
                    ctx.arc(p.x, p.y, s.radius, 0, 2 * Math.PI);
                    ctx.closePath();
                    ctx.fill();
                    // ctx.restore();
                }
            }
        
            Bloom = function(tree, point, figure, color, alpha, angle, scale, place, speed) {
                this.tree = tree;
                this.point = point;
                this.color = color || 'rgb(255,' + random(0, 255) + ',' + random(0, 255) + ')';
                this.alpha = alpha || random(0.3, 1);
                this.angle = angle || random(0, 360);
                this.scale = scale || 0.1;
                this.place = place;
                this.speed = speed;
        
                this.figure = figure;
            }
            Bloom.prototype = {
                setFigure: function(figure) {
                    this.figure = figure;
                },
                flower: function() {
                    var s = this;
                    s.draw();
                    s.scale += 0.1;
                    if (s.scale > 1) {
                        s.tree.removeBloom(s);
                    }
                },
                draw: function() {
                    var s = this, ctx = s.tree.ctx, figure = s.figure;
        
                    ctx.save();
                    ctx.fillStyle = s.color;
                    ctx.globalAlpha = s.alpha;
                    ctx.translate(s.point.x, s.point.y);
                    ctx.scale(s.scale, s.scale);
                    ctx.rotate(s.angle);
                    ctx.beginPath();
                    ctx.moveTo(0, 0);
                    for (var i = 0; i < figure.length; i++) {
                        var p = figure.get(i);
                        ctx.lineTo(p.x, -p.y);
                    }
                    ctx.closePath();
                    ctx.fill();
                    ctx.restore();
                },
                jump: function() {
                    var s = this, height = s.tree.height;
        
                    if (s.point.x < -20 || s.point.y > height + 20) {
                        s.tree.removeBloom(s);
                    } else {
                        s.draw();
                        s.point = s.place.sub(s.point).div(s.speed).add(s.point);
                        s.angle += 0.05;
                        s.speed -= 1;
                    }
                }
            }
        
            window.random = random;
            window.bezier = bezier;
            window.Point = Point;
            window.Tree = Tree;
        
        })(window);
        </script>
        <script>
            function playAudio() {
                var audio = document.getElementById("myAudio");
                audio.play();
            }
        </script>
	    <style>
         body {
            margin: 0;
            padding: 0;
            background-image: url('./img2.png');
            background-size: cover;
            background-repeat: no-repeat;
            font-size: 14px;
            font-family: sans-serif;
            color: white;
            overflow: auto;
          }
          a {
            color: white;
            font-size: 14px;
          }
          #main {
            width: 100%;
          }
          #wrap {
            position: relative;
            margin: 0 auto;
            width: 1100px;
            height: 680px;
            margin-top: 10px;
          }
          #text {
            width: 272px;
            height: 560px;
            left: 188px;
            top: 80px;
            position: absolute;
          }
          #code {
            display: none;
            color: rgb(196, 255, 255);
            font-size: 16px;
            margin-top: 70px;
            line-height: 25px;
            font-size: larger;
            font-weight: bolder;
          }
          #clock-box {
            position: absolute;
            left: 60px;
            top: 550px;
            font-size: 28px;
            display: none;
          }
          #clock-box a {
            font-size: 28px;
            text-decoration: none;
          }
          #clock {
            margin-left: 48px;
          }
          #clock .digit {
            font-size: 64px;
          }
          #canvas {
            margin: 0 auto;
            width: 1100px;
            height: 680px;
          }
          #error {
            margin: 0 auto;
            text-align: center;
            margin-top: 60px;
            display: none;
          }
          .hand {
            cursor: pointer;
          }
          .say {
            margin-left: 5px;
          }
          .space {
            margin-right: 150px;
          }
          
          #message-box{
            position: absolute;
            margin-top:450px;
            font-size: 25px;
            font-family: monospace;
          
          }
        </style>
</head>
    <body>
        <div id="main">
            <div id="error">，<a href="http://www.google.cn/chrome/intl/zh-CN/landing_chrome.html?hl=zh-CN&brand=CHMI">Chrome</a>(<a href="http://firefox.com.cn/download/">Firefox</a>)</div>
            <audio autoplay="autoplay" height="100" width="100" id = "myAudio">
                    <source src="aud.mp3" type="audio/mp3" />
                    <embed height="100" width="100" src="aud.mp3" />
            </audio>
            <div id="wrap">
                <div id="text">
                    <div id="code">
                      <span class="say"> Happiest Birthday  </span><br>
                      <span class="say">Beautiful🫀 </span><br>             
                      <span class="say">MAY GOD GIVE YOU</span><br>
                      <span class="say">ALL THE THINGS YOU WANT AND SUCCESS🥰</span><br>
                      <span class="say">ENJOY YOUR DAY TO THE FULLEST💕</span><br>
                      <span class="say">AUR HAAN PARTY JARUR OKIEE NAH </span><br>
                      <span class="say">Your @aLEIN🫶! </span><br>
                      <span class="say"><span class="space"></span></span> </font>
                          <br />
                          <br />
                      </p>
                    </div>
                  </div>

                  <div id = "message-box"></div>
                <div id="clock-box">
                    <span class="STYLE1"></span><font color="#33CC00"></font>
<span class="STYLE1"></span>
                  <div id="clock"></div>
              </div>
                <canvas id="canvas" width="1100" height="680"></canvas>
            </div>
            
        </div>
    
    <script>
    </script>

    <script>
    (function(){
        var canvas = $('#canvas');
		
        if (!canvas[0].getContext) {
            $("#error").show();
            return false;        }

        var width = canvas.width();
        var height = canvas.height();        
        canvas.attr("width", width);
        canvas.attr("height", height);
        var opts = {
            seed: {
                x: width / 2 - 20,
                color: "rgb(190, 26, 37)",
                scale: 2
            },
            branch: [
                [535, 680, 570, 250, 500, 200, 30, 100, [
                    [540, 500, 455, 417, 340, 400, 13, 100, [
                        [450, 435, 434, 430, 394, 395, 2, 40]
                    ]],
                    [550, 445, 600, 356, 680, 345, 12, 100, [
                        [578, 400, 648, 409, 661, 426, 3, 80]
                    ]],
                    [539, 281, 537, 248, 534, 217, 3, 40],
                    [546, 397, 413, 247, 328, 244, 9, 80, [
                        [427, 286, 383, 253, 371, 205, 2, 40],
                        [498, 345, 435, 315, 395, 330, 4, 60]
                    ]],
                    [546, 357, 608, 252, 678, 221, 6, 100, [
                        [590, 293, 646, 277, 648, 271, 2, 80]
                    ]]
                ]] 
            ],
            bloom: {
                num: 700,
                width: 1080,
                height: 650,
            },
            footer: {
                width: 1200,
                height: 5,
                speed: 10,
            }
        }

        var tree = new Tree(canvas[0], width, height, opts);
        var seed = tree.seed;
        var foot = tree.footer;
        var hold = 1;

        canvas.click(function(e) {
            playAudio();
            console.log("Helloworld!");
            var offset = canvas.offset(), x, y;
            x = e.pageX - offset.left;
            y = e.pageY - offset.top;
            if (seed.hover(x, y)) {
                hold = 0; 
                canvas.unbind("click");
                canvas.unbind("mousemove");
                canvas.removeClass('hand');
            }
        }).mousemove(function(e){
            var offset = canvas.offset(), x, y;
            x = e.pageX - offset.left;
            y = e.pageY - offset.top;
            canvas.toggleClass('hand', seed.hover(x, y));
        });
        
        

        var seedAnimate = eval(Jscex.compile("async", function () {
            seed.draw();
            while (hold) {
                $await(Jscex.Async.sleep(10));
            }
            while (seed.canScale()) {
                seed.scale(0.95);
                $await(Jscex.Async.sleep(10));
            }
            while (seed.canMove()) {
                seed.move(0, 2);
                foot.draw();
                $await(Jscex.Async.sleep(10));
            }
        }));

        var growAnimate = eval(Jscex.compile("async", function () {
            do {
    	        tree.grow();
                $await(Jscex.Async.sleep(10));
            } while (tree.canGrow());
        }));

        var flowAnimate = eval(Jscex.compile("async", function () {
            do {
    	        tree.flower(2);
                $await(Jscex.Async.sleep(10));
            } while (tree.canFlower());
        }));

        var moveAnimate = eval(Jscex.compile("async", function () {
            tree.snapshot("p1", 240, 0, 610, 680);
            while (tree.move("p1", 500, 0)) {
                foot.draw();
                $await(Jscex.Async.sleep(10));
            }
            foot.draw();
            tree.snapshot("p2", 500, 0, 610, 680);

            canvas.parent().css("background", "url(" + tree.toDataURL('image/png') + ")");
            canvas.css("background", "#ffe");
            $await(Jscex.Async.sleep(300));
            canvas.css("background", "none");
        }));

        var jumpAnimate = eval(Jscex.compile("async", function () {
            var ctx = tree.ctx;
            while (true) {
                tree.ctx.clearRect(0, 0, width, height);
                tree.jump();
                foot.draw();
                $await(Jscex.Async.sleep(25));
            }
        }));

        var textAnimate = eval(Jscex.compile("async", function () {
		    var together = new Date();
		    together.setFullYear(2002, 25, 12); 			//时间年月日
		    together.setHours(20);						//小时	
		    together.setMinutes(0);					//分钟
		    together.setSeconds(0);					//秒前一位
		    together.setMilliseconds(2);				//秒第二位

		    $("#code").show().typewriter();
            $("#clock-box").fadeIn(500);
            while (true) {
                timeElapse(together);
                $await(Jscex.Async.sleep(1000));
            }
        }));

        var runAsync = eval(Jscex.compile("async", function () {
            $await(seedAnimate());
            $await(growAnimate());
            $await(flowAnimate());
            $await(moveAnimate());

            textAnimate().start();

            $await(jumpAnimate());
        }));

        runAsync().start();
    })();
    </script></body></html>
