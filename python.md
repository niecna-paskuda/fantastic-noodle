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
</table>