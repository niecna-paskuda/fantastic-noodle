# Python

## Best practises

### Code style

_PEP_ stands for a _Python Enhancement Proposal_. [PEP8](https://www.python.org/dev/peps/pep-0008/) is a coding style guide, setting out coding conventions for: naming, comments, whitespaces, code lay-out and so on.

### Checkers & linters

<table>
  <thead>
    <tr>
      <th style="text-align:left">tool</th>
      <th style="text-align:left">what it does</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><a href="https://www.pylint.org/">pylint</a>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>checks for errors,</li>
          <li>detects code smells,</li>
          <li>enforces coding standard (close to PEP8),</li>
          <li>gives overall mark for the code analysed,</li>
          <li>recommends suggestions about refactors.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://pypi.org/project/pyflakes/">pyflakes</a>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>examines the files individually = faster than pylint, but limited in the
            checks,</li>
          <li>no style checking,</li>
          <li>checks for errors,</li>
          <li>&#x2753; code smells detection</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://pypi.org/project/flake8/">Flake8</a>
      </td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>incorporates different tools:
            <ul>
              <li><a href="https://pypi.org/project/pycodestyle/">pycodestyle</a> (PEP8 checks),</li>
              <li><a href="https://pypi.org/project/pyflakes/">pyflakes</a> (see above),</li>
              <li><a href="https://github.com/PyCQA/mccabe">McCabe complexity checker</a>.</li>
            </ul>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/hhatto/autopep8">autopep8</a>
      </td>
      <td style="text-align:left">uses pycodestyle to automatically conform to PEP8.</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/python/mypy">mypy</a>
      </td>
      <td style="text-align:left">optional static type checker</td>
    </tr>
  </tbody>
</table>On integrations with vim see here.

## Debugging

On integrations with vim see here.

### PDB

{% embed url="https://docs.python.org/3/library/pdb.html" %}

Starting it:

* python console: `import pdb; pdb.run('afunction()')`
* shell: `python3 -m pdb somescript.py`
* from code: `import pdb; pdb.set_trace()`

Using it: [a simple session with pdb](https://realpython.com/python-debugging-pdb/).

Pdb itself is not inviting to use, the presentation without any color makes the lines blend into one another.

❓ Does it have any limitation when it comes to debugging frameworks \(and code involving browser requests\)?

### PUDB

{% embed url="https://documen.tician.de/pudb/" %}


